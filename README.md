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
/* Items are in line */
flex-direction: row-reverse;
/* The items are in reverse row, i.e. 3, 2, 1. */
flex-direction: column;
/* The items are in a single column, one below the other. */
flex-direction: column-reverse;
/* The items are in a single column, one below the other, but in reverse order: 3, 2 and 1. */
```

## 3. flex-wrap

Defines whether items should break the line or not. By default they do not break lines, this causes flex items to be compressed beyond the content limit.

This is usually a property that is almost always set to flex-wrap: wrap; So when one of the flex items reaches the content limit, the last item moves to the column below and so on.

```css
flex-wrap: nowrap;
/* Default value, does not allow line breaks. */
flex-wrap: wrap;
/* Break the line as soon as one of the flex items can no longer be compressed. */
flex-wrap: wrap-reverse;
/* Break the line as soon as one of the flex items can no longer be compressed. The break is in the opposite direction, that is, towards the line above. */
```

## 4. flex-flow

flex-flow is a shortcut for the flex-direction and flex-wrap properties. You won't see it used much, because generally when we change flex-direction to column, we keep the flex-wrap default, which is nowrap.

And when we change flex-wrap to wrap, we keep the flex-direction default, which is row.

```css
flex-flow: row nowrap;
/* Puts the content in line and does not allow line breaks. */
flex-flow: row wrap;
/* Puts the content in line and allows line wrapping. */
flex-flow: column nowrap;
/* Places the content in a column and does not allow line breaks. */
```

## 5. justify-content

Aligns the flex items in the container according to the direction. The property only works if the current items do not occupy the entire container. This means that when setting flex: 1; or something similar in the items, the property will no longer have a function.

Excellent property to be used in cases where you want to align one item on the left and another on the right, as in a simple header with branding and navigation.

```css
justify-content: flex-start;
/* Aligns items to the beginning of the container. */
justify-content: flex-end;
/* Aligns items to the end of the container. */
justify-content: center;
/* Aligns items to the center of the container. */
justify-content: space-between;
/* Creates equal spacing between elements. Keeping the first one stuck at the beginning and the last one at the end. */
justify-content: space-around;
/* Creates spacing between elements. The middle spacings are twice as wide as the initial and final ones. */
```

## 6. align-items

`align-items` aligns flex items according to the container axis. The alignment is different for when items are in columns or rows.

This property allows for the long-awaited central alignment on the vertical axis, something that was previously only possible with different hacks.

```css
align-items: stretch;
/* Default value, which makes flex items grow equally. */
align-items: flex-start;
/* Aligns items to the beginning. */
align-items: flex-end;
/* Aligns items to the end. */
align-items: center;
/* Aligns items to the center. */
align-items: baseline;
/* Aligns items according to the typography baseline. */
```

## 7. align-content

Aligns the container lines in relation to the vertical axis. The property only works if there is more than one row of flex-items. To do this, the flex-wrap needs to be wrapped.

Furthermore, its effect will only be seen if the container is larger than the sum of the item lines. This means that if you don't define height for the container, the property has no influence on the layout.

```css
align-content: stretch;
/* Default value, which makes flex items grow equally vertically. */
align-content: flex-start;
/* Align all item lines to the beginning. */
align-content: flex-end;
/* Align all item lines to the end. */
align-content: center;
/* Aligns all item lines to the center. */
align-content: space-between;
/* Creates equal spacing between lines. Keeping the first one stuck to the top and the last one to the bottom. */
align-content: space-around;
/* Creates spacing between lines. The middle spacings are twice as wide as the top and bottom. */
```
