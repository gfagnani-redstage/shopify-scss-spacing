# Shopify SCSS spacing

## About

This library helps to create a default and reusable styles for margins and paddings following the [Blocks, Elements and Modifiers](http://getbem.com/introduction/) style naming.

It's a integration with [Shopify Grid System](https://www.shopify.com/partners/blog/css-grid) and the [Bootstrap Spacing](https://getbootstrap.com/docs/4.3/utilities/spacing/) utilities. For example:

## Install

Import the file _spacing.scss in the end of the file style.scss.

```sass
    @import 'spacing';
```
## Configure

Inside of the _spacing.scss there are some options to customize. First of all, there is a variable $spacings-range where contains the sizes. For example:

```sass
    $spacings-range : (0,5,10); // It's means you'll have the utilities only on those sizes (0px, 5px and 10px).
```

In the second point is, there is a variable $grid-breakpoint-has-spacings where contains the grid breakpoints to compile.

```sass
    $grid-breakpoint-has-spacings :($small, $medium); // It's means you'll have the utilities just for small and medium width.
```

## Usage

There are some examples below:

1 - An element with margin on the top of 10px: 

```html
    <div class="example-element mt-10">
        Spacings
    </div>
```
2 - An element with padding on the left of 40px: 

```html
    <div class="example-element pl-40">
        Spacings
    </div>
```

3 - An element with margin on the top of 20px only on medium screen according of Shopify Grid Breakpoint's sizes:

```html
    <div class="example-element medium--mt-20">
        Spacings
    </div>
```

4 - An element with padding on the bottom of 30px and also 50px only on large screen according of Shopify Grid Breakpoint's sizes:

```html
    <div class="example-element pb-30 large-up--pb-50">
        Spacings
    </div>
```

## Documentation

As you can see the examples above, the classes follow this format: 

```html
{property}{sides}-{size}
```
Or
```html
{grid-breakpoint}--{property}{sides}-{size}
```

### Grid Breakpoint

You can use the following breakpoints: 

Parameter     | Width                 | Example
------------- | ----------------------|------
Empty         | < 750px               | mt-10
medium--      | \>= 750px and < 990px | medium--mt-10
large-up--    | \>= 990px             | large-up--mt-10

Attention: the width can be different according your grid settings.

### Property

You can use the following properties:

Parameter     | CSS Propriety | Example
------------- | --------------|-------- 
m             | margin        | ml-10
p             | padding       | pl-10

### Sides

You can use the following sides:

Parameter     | Side         | Example
------------- | -------------|--------
t             | top          | mt-15
r             | right        | mr-15
b             | bottom       | mb-15
l             | left         | ml-15

### Sizes

You can use the following sizes:

Parameter     | Size         | Example
------------- | -------------|--------
0             | 0px          | pt-0
10            | 10px         | pt-10
15            | 15px         | pt-15
20            | 20px         | pt-20
...           | ...          | ...

Attention: the sizes can be different according your size settings.








