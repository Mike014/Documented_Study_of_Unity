### What is a Vector?

* Unity uses a 3D coordinate system (X, Y, Z).
* The combination of these three values ​​forms a **Vector**.
* A vector can represent:

* **Position**
* **Direction**
* **Scale**
* **Rotation**

### Vectors in Unity

* Each GameObject has a **Transform** component with three properties: **Position**, **Rotation**, **Scale**.
* In C#, these are represented by a **Vector3** (x, y, z).

### Creating and Using a Vector3

* You can declare a vector, for example:

```csharp
Vector3 newPosition = new Vector3(1, 0, -2);

transform.position = newPosition;
```
* This moves the Cube to the new position.

### Vector Operators

* You can use operators like `+=` to move an object relative to its current position:

```csharp
Vector3 movement = new Vector3(1, 0, 1);
transform.position += movement;
```

### Movement with Update

* Using `Update()`, the object can be moved continuously:

```csharp
void Update()
{
transform.position += new Vector3(1, 0, 0);
}
```
* This, however, depends on the number of frames per second, so it is not precise.

### Using Time.deltaTime

* To make the movement independent of the frame rate, multiply by `Time.deltaTime`:

```csharp
void Update()
{
transform.position += new Vector3(1, 0, 0) * Time.deltaTime;
}
```
* This way the Cube moves **at a constant speed (1 meter/second)** on any device.