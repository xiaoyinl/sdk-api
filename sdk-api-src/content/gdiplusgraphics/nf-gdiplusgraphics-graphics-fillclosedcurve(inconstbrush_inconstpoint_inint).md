---
UID: NF:gdiplusgraphics.Graphics.FillClosedCurve(IN const Brush,IN const Point,IN INT)
title: Graphics::FillClosedCurve(IN const Brush,IN const Point,IN INT) (gdiplusgraphics.h)
description: The Graphics::FillClosedCurve method creates a closed cardinal spline from an array of points and uses a brush to fill the interior of the spline.
old-location: gdiplus\_gdiplus_CLASS_Graphics_FillClosedCurve_Brush_brush_Point_points_INT_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsfillclosedcurvemethods\fillclosedcurve.htm
ms.date: 12/05/2018
ms.keywords: FillClosedCurve, FillClosedCurve method [GDI+], FillClosedCurve method [GDI+],Graphics class, Graphics class [GDI+],FillClosedCurve method, Graphics.FillClosedCurve, Graphics.FillClosedCurve(IN const Brush,IN const Point,IN INT), Graphics.FillClosedCurve(const Brush*,const Point*,INT), Graphics::FillClosedCurve, Graphics::FillClosedCurve(IN const Brush,IN const Point,IN INT), _gdiplus_CLASS_Graphics_FillClosedCurve_Brush_brush_Point_points_INT_count_, gdiplus._gdiplus_CLASS_Graphics_FillClosedCurve_Brush_brush_Point_points_INT_count_
f1_keywords:
- gdiplusgraphics/Graphics.FillClosedCurve
dev_langs:
- c++
req.header: gdiplusgraphics.h
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
- Graphics.FillClosedCurve
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# Graphics::FillClosedCurve(IN const Brush,IN const Point,IN INT)


## -description


The <b>Graphics::FillClosedCurve</b> method creates a closed cardinal spline from an array of points and uses a brush to fill the interior of the spline. 


## -parameters




### -param brush [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush">Brush</a>*</b>

Pointer to a 
					<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush">Brush</a> object that is used to paint the interior of the spline. 


### -param points [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>*</b>

Pointer to an array of points that this method uses to create a closed cardinal spline. Each point in the array is a point on the spline. 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of points in the 
					<i>points</i> array. 


## -returns



Type: <strong>Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-cardinal-splines-about">Cardinal Splines</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-drawing-cardinal-splines-use">Drawing Cardinal Splines</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-open-and-closed-curves-about">Open and Closed Curves</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush">SolidBrush</a>
 

 

