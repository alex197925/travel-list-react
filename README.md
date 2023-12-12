<!-- @format -->

## Travel list react.js app

## Learning tree

1. Add style conditionally
2. Work with forms (controlled elements)
3. Lifting state up ( https://www.youtube.com/watch?v=rdwc4JmX_fU )
4. Child, parents communication (inverse data flow)
5. Toggling items.
   ### Pass functions from parent to the child as a props

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

```
 function handleDeleteItem(id) {
    setItems((items) => items.filter((item) => item.id !== id));
  }
```

7. Update items

```
 function handleAddItems(item) {
    setItems((items) => [...items, item]);
  }

```
