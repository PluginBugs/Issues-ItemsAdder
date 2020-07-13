# Erreurs courantes

## I see only a white square

If you see a **white square** make sure the **height** of your image is not **greather** than the `y_position` value you set. To **bypass** that create an **image** with **higher height**.

## My partially transparent image looks "cut"

Minecraft cuts images if they have transparency \(0/255 alpha channel value\), so you must set 1/255 transparency in order to avoid Minecraft to cut it

## When I add a hud others shift of some pixels

Be sure to have each image size set to a multiple of 2.  
Example:  
- 2x2  
- 4x4  
- 6x6  
- 52x52  
- ......  


If you still have problems try to increase/decrease the size by 2 until the wrong shift disappears.  


