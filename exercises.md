## অনুশীলন  # ১

Design a class named Point which will model a 2D point with `X` and `Y` coordinates. 

1. Two instance variable variables `X` (`int`) and `X` (`int`)
2. A "_no-argument_" (or "_no-arg_") constructor that construct a point at `(0, 0)`.
3. A constructor that constructs a point with the given `x` and `y` coordinates.
4. Getter and setter for the instance variables `x` and y.
5. A method `setXY()` to set both x and y.
6. A `toString()` method that returns a string description of the instance in the format `"(x,
y)"`.
7. A method called `distance(int x, int y)` that returns the distance from this point to
another point at the given `(x, y)` coordinates.
8. An overloaded `distance(Point another)` that returns the distance from this point to
the given `Point` instance another.

For example - 
```java
package bd.com.howtocode.java;

/**
 * @author Bazlur Rahman Rokon
 * @date 6/19/15.
 */

public class Point {
    private int x;
    private int y;

    public Point() {
        x = 0;
        y = 0;
    }

    public Point(int x, int y) {
        this.x = x;
        this.y = y;
    }

    public int getX() {
        return x;
    }

    public void setX(int x) {
        this.x = x;
    }

    public int getY() {
        return y;
    }

    public void setY(int y) {
        this.y = y;
    }

    public double distance(int x, int y) {
        int xDiff = this.x - x;
        int yDiff = this.y - y;
        return Math.sqrt(xDiff * xDiff + yDiff * yDiff);
    }

    public double distance(Point p2) {
        return distance(p2.getX(), p2.getY());
    }

    @Override
    public String toString() {
        return "(" + x + ", " + ")";
    }
}
```

Now write a program that allocates 10 points in an array of `Point`, and initializes to (1, 1), (2,
2), ... (10, 10).