# Flex Container

The Flex Container is the tag that surrounds the flex items, when indicating display: flex, this tag becomes a Flex Container.

## 1. display

Defines the element as a flex container, making its children flex-items.

```css
display: flex;
display: inline-flex;
/* Makes the element a flex container by automatically transforming all of its direct children into flex items.*/
```

## 2. flex-direction

Sets the direction of flex items. By default it is row, so when display: flex; is added, the elements are in line, next to each other.
The change from row to column usually happens when we are defining styles in media queries for mobile. This ensures that the content is presented in a single column.

```css
flex-direction: row;
/*  Items are in line */
flex-direction: row-reverse;
/*  The items are in reverse row, i.e. 3, 2, 1. */
flex-direction: column;
/*  The items are in a single column, one below the other. */
flex-direction: column-reverse;
/*  The items are in a single column, one below the other, but in reverse order: 3, 2 and 1. */
```
