# Section

Point2D(float x, y)
 .x = x
 .y = y

Rect r:
 .x
 .y
 .x2
 .y2

 in(Rect r, Point2D p):
  r.x < p.x < r.x2 && r.y < p.y < r.y2

 USING section principle

// in section has context: r,p
// context principle
// function can have arguments and also can have context
 section in(x1, _in_, x2):
  r.x1 < p._in_ < r.x2

in(Rect r, Point2D p):
   in(x, x, x2) && in(y, y, y2)
