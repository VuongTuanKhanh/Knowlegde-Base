# Vector

## Definition
- Vector is an object, or a list of attributes that move around space.
- Two main properties of a Vector:
    - Length
    - Direction

## Operations
- **Addition:**
    - **Associative**:

        ![Associative Addition](../Image/Associative.jpg)

    - **Method**: Add up the components of two vector
        
        ![Addition](../Image/Addition.jpg)

        ![Substract](../Image/Substract.jpg)

- **Multiplication by a Scalar:**
    - **Method**: Multiple the components of the vector with the Scalar
        
        ![Scalar Multiple](../Image/Scalar_Mul.jpg)

        - `r` and `ar` ( with a is `a` Scalar ) will have the same direction if `a` is position.

- **Size of a Vector (Length):**
    - **Method:** Size of a Vector equal to the sum of the squares of its components.

        ![Vector Size](../Image/Vector_Size.jpg)

- **Dotted product of two Vector:**
    - **Method:** Multiplying the first component of two Vectors together and then add it to the result of multiplying the second component of two Vectors, return a scalar number.
        - The result will be a Scalar number.
        ![Dotted](../Image/Dotted_1.jpg)
        ![Dotted](../Image/Dotted_2.jpg)
        
        - **Commutitive**:

            ![Commutitive](../Image/Dotted_3.jpg)

        - **Distributive over addition:**

            ![Distribute](../Image/Distribute.jpg)

        - **Associative over Scalar multiplication:**

            ![Associative Scalar](../Image/Associative_Scalar.jpg)

- **Relationship between the dot product and the length (modulus) of a vector:**
    - If we want to get the size of a Vector, we dotting the Vector with itself and taking the square root.

    ![Dotted vs Size](../Image/Dotted_vs_Size.jpg)

- **Cosine and Dot product:**
    - **Use case:** The Dot product with the Cosine shows us whether the two Vectors go in the same direction. To check for the angle between two vector, use `cos`.

        ![Dotted vs Cos](../Image/Dot_vs_Cos.jpg)

- **Projection:**
    - **Projection** is the shadow of `s` on `r` ( **perpendicular** )
    - `rs` divide the length of `r` will give us the scalar projection of `s` ( `|s|cos(Θ)` ) on `r` times the size of `r`.
    
        ![Projection](../Image/Projection.jpg)
        ![Projection](../Image/Projection_1.jpg)

        - The **Projection** is: 
        
            ![Projection](../Image/Projection_2.jpg)
    
    - **Vector Projection:**
        - Check how much `s` go along with `r`

            ![Vector Projection](../Image/Vector_Projection.jpg)

    - **Change Basic:**
        - *Must first check whether the new 2 axies are orthogonal*
        - Find the projection of the vector on the original co-ordinate system on the new co-ordinate system.

    - **Linear Independence:**
        - Vectors are not lie in the same plane span