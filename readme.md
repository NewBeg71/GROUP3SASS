# What is @extend?

@extend is a feature of Sass that allows classes to share a set of properties
with one another. Selectors that @extend a class in Sass will have their selector
included right up next to the class it is extending, resulting in a comma separated
list.
<hr>
##### Its syntax looks like so:
```scss

  @extend .class-name;

```
<hr>

##### Using @extend looks like so:
```scss

.foo {
  color: black;
  border: 1px solid black;
}

.bar {
  @extend .foo;
  background-color: red;
}

```
<hr>

##### This is compiled to:
```scss
.foo, .bar {
  color: black;
  border: 1px solid black;
}

.bar {
  background-color: red;
}
```
<hr>

# Advantages of @extend:

### Cleaner HTML Classes
As you can see in the second case study, using so many classes in one element
may make it hard to determine the root cause if you run into issues. The structure
of HTML tags also does not look very nice and clean.

### Reducing Duplication of CSS
In web development, we always have some duplication within our CSS styles. Hence,
reusing written CSS source code can be extremely necessary. @extend can help us
reuse our CSS when it is appropriate and cleaner to do so.

### Saving time and effort
Developers can reuse CSS for various elements, reducing the effort needed to find
the root cause of CSS issues and making their CSS structure nice and clean.

[Resource:](https://www.sitepoint.com/the-benefits-of-inheritance-via-extend-in-sass/)
