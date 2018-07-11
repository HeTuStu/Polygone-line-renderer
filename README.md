
	I created a ColoredDrawable class which extends DrawableDecorator to draw out white margins between each panels. 
  Then I wrote DDALineRenderer, BresenhamLineRenderer, AlternatingLineRenderer, and AntialiasingLineRender in order to draw lines for first three pages. 
  Corresponding test pages Parallelogram was made for page 2. Then RandomPolygon test was made for page 3. 
	I have put majority of efforts on page 4 and page 5 for polygons drawing. 
  I wrote FilledPolygonRenderer for any shape of polygons drawing. 
  In total, I have separate polygons into 4 big categories: Horizontal Top line polygons, Horizontal Bottom line polygons, 
  Non-horizontal lines polygons with left line shorter, Non-horizontal lines polygons with right line shorter. 
  Among these 4 categories, I have separated 3 sub-categories for each: top/bottom vertex in middle, left or right of the other two vertices. 
  Using a function called fillPixels_leftToRight to draw from left to right. 
	Then corresponding polygon renderer test pages StarburstPolygonTest, MeshPolygonTest and RandomPolygonTest were made. 
  There is a main issue that I put lots of time in but cannot fix, when turned to page 5, it is easy to see there are polygons that are overlapping. 
  Especially in the middle of the starburstPolygon. Same thing happened to MeshpolygonTest, there were overlapping that can see visually between some horizontal lines. 
  I first suspect the problem was caused by drawing of polygons with horizontal line. So I added if statement to fix it, 
  but main problem still occurs. Then I suspect it is because of the rounding of double type to int type, 
  in which lost information. However, I still cannot really fix it.
