<!-- @format -->

## Travel list react.js app

## Learning tree

1. Add style conditionally
2. Work with forms (controlled elements)
3. Lifting state up ( https://www.youtube.com/watch?v=rdwc4JmX_fU )
4. Child, parents communication (inverse data flow)
5. Toggling items.
   ### Pass handleToggleItem function from parent to the child

```
 function handleToggleItem(id) {
    setItems((items) =>
      items.map((item) =>
        item.id === id ? { ...item, packed: !item.packed } : item
      )
    );
  }
```

6. Delete items
7. Update items
