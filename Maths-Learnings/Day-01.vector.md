## Vector

A vector is a quantity that has both magnitude and direction and represents a displacement or movement in space.

### Magnitude (Length) of vector

Magnitude is the size, length, or amount of a quantity, regardless of its direction.

If a vector is

[
\mathbf{v} = (x, y)
]

then its magnitude is

magnitude = (x^2 + y^2)^(1/2)

### Vector Addition

Suppose

A=(2,3)

B=(5,1)

Add coordinate-wise

(2+5,3+1) = (7,4)

### Vector Subtraction

Suppose

A=(10,8)

B=(4,3)

Subtract

(10−4, 8−3) = (6,5)

### Scalar Multiplication

Scalar simply means "A normal number."

Example

3 × (2,5) -- 3 is scaler which scales vector by 3 quantity

Multiply every coordinate.

(6,15)

### Unit Vector

Suppose

v=(3,4)

Length = 5

Divide every coordinate by 5.

(3/5,4/5)

Now
Length = 1

This is called a unit vector.

### Why normalize?

Imagine comparing two arrows:

100 meters north

1 meter north

Their lengths differ a lot, but the direction is the same. By converting them to unit vectors, algorithms compare orientation instead of raw size.

### Distance Between Two Points

Suppose

A=(2,5)

B=(7,9)

Subtract

(5,4)

Length

√(25+16) = √41  ===  ((x2 -x1)^2 + (y2-y1)^2)^(0.5)

Distance

√41

| Operation             | Formula     | Example              |
| --------------------- | ----------- | -------------------- |
| Addition              | (a,b)+(c,d) | (a+c,b+d)            |
| Subtraction           | (a,b)-(c,d) | (a−c,b−d)            |
| Scalar Multiplication | k(a,b)      | (ka,kb)              |
| Magnitude             | √(x²+y²)    | (3,4)=5              |
| Unit Vector           | v / ||v||   | (3/5,4/5)            |
| Distance              | ||A−B||     | √((x₂−x₁)²+(y₂−y₁)²) |
