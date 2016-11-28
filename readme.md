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
