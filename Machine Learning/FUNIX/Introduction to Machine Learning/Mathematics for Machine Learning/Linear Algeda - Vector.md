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
        - `2r[a,b] = r[2a,2b]`
        - `r[a, b] - r[a,b] = r[0,0]`
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

        - Distributive over addition:

            ![Distribute](../Image/Distribute.jpg)