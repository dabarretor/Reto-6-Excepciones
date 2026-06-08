# Reto 6

1. Add the required exceptions in the Reto 1 code assigments.

- [Ejercicio_1](reto1/punto1.py)

- [Ejercicio_2](reto1/punto2.py)

- [Ejercicio_3](reto1/punto%203.py)

- [Ejercicio_4](reto1/punto4.py)

- [Ejercicio_5](reto1/punto%205.py)

---

2. In the package Shape identify at least cases where exceptions are needed (maybe when validate input data, or math procedures) explain them clearly using comments and add them to the code.

- [Solución_del_punto_2:clase.shape](Paquete.Shape/shape.py)

- [Solución_del_punto_2:clase.Triangle](Paquete.Shape/Triangle.py)

- [Solución_del_punto_2:clase.Rectangle](Paquete.Shape/Rectangle.py)

- [Prueba_del_funcionamiento:main](Paquete.Shape/main.py)

## Diagrama de clases

```mermaid
classDiagram

class Shape {
    +is_regular : bool
    +vertices: list(Point)
    +edges: list(Line)
    +inner_angles: list(float)
    +compute_area(self)
    +compute_perimeter(self)
    +compute_inner_angles(self)
}

class Point {
    +x : int
    +y : int
    +compute_distance(self, Point)
}

class Line {
    +start_point : Point
    +end_point : Point
    +length : float
}


class Rectangle {
}

class Isosceles {
}

class Equilateral { 
}

class Scalene {   
}

class TriRectangle {
}

class Square {
}

Triangle <|-- TriRectangle
Triangle <|-- Isosceles
Triangle <|-- Equilateral
Triangle <|-- Scalene

Rectangle <|-- Square

Shape <|-- Rectangle
Shape <|-- Triangle
Shape *-- Line
Shape *-- Point
```