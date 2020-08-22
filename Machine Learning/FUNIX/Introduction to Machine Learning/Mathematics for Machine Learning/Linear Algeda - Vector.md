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

- **Multiplication by a Scalar:**
    - **Method**: Multiple the components of the vector with the Scalar
        
        ![Scalar Multiple](../Image/Scalar_Mul.jpg)

        ![Substract](../Image/Substract.jpg)

        - `r` and `ar` ( with a is `a` Scalar ) will have the same direction if `a` is position.

- **Size of a Vector (Length):**
    - **Method:** Size of a Vector equal to the sum of the squares of its components.

        ![Vector Size](../Image/Vector_Size_1.jpg)
        ![Vector Size](../Image/Vector_Size_2.jpg)

- **Dotted product of two Vector:**
    - **Method:** Multiplying the first component of two Vectors together and then add it to the result of multiplying the second component of two Vectors.
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
    - **Use case:** The Dot product with the Cosine shows us whether the two Vector go in the same direction.
        - The result will be between 0 and 1.

            ![Dotted vs Cos](../Image/Dot_vs_Cos.jpg)