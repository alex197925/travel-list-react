<!-- @format -->

## Travel list react.js app

## Learning tree

1. Add style conditionally
2. Work with forms (controlled elements)
3. Lifting state up ( https://www.youtube.com/watch?v=rdwc4JmX_fU )
4. Child, parents communication (inverse data flow)

# A. Toggling items.

```
 function handleToggleItem(id) {
    setItems((items) =>
      items.map((item) =>
        item.id === id ? { ...item, packed: !item.packed } : item
      )
    );
  }
```

# B. Delete items

```
 function handleDeleteItem(id) {
    setItems((items) => items.filter((item) => item.id !== id));
  }
```

# C. Update items

```
 function handleAddItems(item) {
    setItems((items) => [...items, item]);
  }

```

5. Derived state
   ![](image/Screenshot2023-12-12at13.19.43.png)
