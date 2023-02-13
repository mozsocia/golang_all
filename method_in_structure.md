teach me method of structure in golang

In Go, structures are used to group together values with different data types under a single name. Here's how you can define and use structures in Go:

```go
type Person struct {
    name string
    age int
    address string
}

func main() {
    var p Person
    p.name = "John Doe"
    p.age = 30
    p.address = "123 Main St."

    fmt.Println("Name:", p.name)
    fmt.Println("Age:", p.age)
    fmt.Println("Address:", p.address)
}

```

In this example, we've defined a structure called `Person` that has three fields: `name`, `age`, and `address`. To create a new structure, we can use the following syntax:

```go
p := Person{name: "Jane Doe", age: 25, address: "456 Main St."}

```

We can also create a new structure using the new keyword:

```go
p := new(Person)
p.name = "Jane Doe"
p.age = 25
p.address = "456 Main St."

```

You can access the fields of a structure using the dot notation, for example: `p.name`. And you can modify the fields using the same notation, for example: `p.name = "Jane Doe"`.

It's also possible to define methods on structures, which allow you to perform actions on the structure's data. Here's an example:

```go
type Person struct {
    name string
    age int
    address string
}

func (p Person) PrintPerson() {
    fmt.Println("Name:", p.name)
    fmt.Println("Age:", p.age)
    fmt.Println("Address:", p.address)
}

func main() {
    p := Person{name: "Jane Doe", age: 25, address: "456 Main St."}
    p.PrintPerson()
}
```
