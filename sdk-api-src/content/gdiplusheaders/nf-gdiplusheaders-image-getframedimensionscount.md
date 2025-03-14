---
UID: NF:gdiplusheaders.Image.GetFrameDimensionsCount
title: Image::GetFrameDimensionsCount (gdiplusheaders.h)
description: The Image::GetFrameDimensionsCount method gets the number of frame dimensions in this Image object.
old-location: gdiplus\_gdiplus_CLASS_Image_GetFrameDimensionsCount_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\getframedimensionscount.htm
ms.date: 12/05/2018
ms.keywords: GetFrameDimensionsCount, GetFrameDimensionsCount method [GDI+], GetFrameDimensionsCount method [GDI+],Image class, Image class [GDI+],GetFrameDimensionsCount method, Image.GetFrameDimensionsCount, Image::GetFrameDimensionsCount, _gdiplus_CLASS_Image_GetFrameDimensionsCount_, gdiplus._gdiplus_CLASS_Image_GetFrameDimensionsCount_
f1_keywords:
- gdiplusheaders/Image.GetFrameDimensionsCount
dev_langs:
- c++
req.header: gdiplusheaders.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Gdiplus.dll
api_name:
- Image.GetFrameDimensionsCount
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# Image::GetFrameDimensionsCount


## -description


The <b>Image::GetFrameDimensionsCount</b> method gets the number of frame dimensions in this 
			<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object.


## -parameters






## -returns



Type: <strong>Type: <b>UINT</b>
</strong>

This method returns the number of frame dimensions in this 
						<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object.




## -remarks



This method returns information about multiple-frame images, which come in two styles: multiple page and multiple resolution. 

A multiple-page image is an image that contains more than one image. Each page contains a single image (or frame). These pages (or images, or frames) are typically displayed in succession to produce an animated sequence, such as in an animated GIF file. 

A multiple-resolution image is an image that contains more than one copy of an image at different resolutions.

Windows GDI+ can support an arbitrary number of pages (or images, or frames), as well as an arbitrary number of resolutions.


#### Examples



The following console application creates an 
						<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object based on a TIFF file. The code calls the <b>Image::GetFrameDimensionsCount</b> method to find out how many frame dimensions the 
						<b>Image</b> object has. Each of those frame dimensions is identified by a 
						GUID, and the call to <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getframedimensionslist">Image::GetFrameDimensionsList</a> retrieves those 
						GUIDs. The first 
						GUID is at index 0 in the 
						<i>pDimensionIDs</i> array. The call to the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getframecount">Image::GetFrameCount</a> method determines the number of frames in the dimension identified by the first 
						GUID.


```cpp
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;

INT main()
{
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   Image* image = new Image(L"Multiframe.tif");

   // How many frame dimensions does the Image object have?
   UINT count = 0;
   count = image->GetFrameDimensionsCount();
   printf("The number of dimensions is %d.\n", count);
   GUID* pDimensionIDs = (GUID*)malloc(sizeof(GUID)*count);

   // Get the list of frame dimensions from the Image object.
   image->GetFrameDimensionsList(pDimensionIDs, count);

   // Display the GUID of the first (and only) frame dimension.
   WCHAR strGuid[39];
   StringFromGUID2(pDimensionIDs[0], strGuid, 39);
   wprintf(L"The first (and only) dimension ID is %s.\n", strGuid);

   // Get the number of frames in the first dimension.
   UINT frameCount = image->GetFrameCount(&pDimensionIDs[0]);
   printf("The number of frames in that dimension is %d.\n", frameCount);
    
   free(pDimensionIDs);
   delete(image);
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```


The preceding code, along with a particular file, Multiframe.tif, produced the following output:


```cpp
The number of dimensions is 1.
The first (and only) dimension ID is {7462DC86-6180-4C7E-8E3F-EE7333A7A483}.
The number of frames in that dimension is 4.
```


You can look up the displayed GUID in Gdiplusimaging.h and see that it is the identifier for the page dimension. So the program output tells us that the file Multiframe.tif has four pages; that is, four frames in the page dimension.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-copying-individual-frames-from-a-multiple-frame-image-use">Copying Individual Frames from a Multiple-Frame Image</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-creating-and-saving-a-multiple-frame-image-use">Creating and Saving a Multiple-Frame Image</a>



<a href="https://docs.microsoft.com/previous-versions/ms534434(v=vs.85)">EncoderParameter</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getframecount">Image::GetFrameCount</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getframedimensionslist">Image::GetFrameDimensionsList</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)">Image::SaveAdd Methods</a>
 

 

