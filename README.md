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

## Derived state comes into play when we need to calculate a value based on existing state or props.

```
function Stats({ items }) {
  // console.log(items.length);

  if (!items.length)
    return (
      <p className='stats'>
        <em>Start adding some items to your packing list 🚀</em>
      </p>
    );


----------------- Derived state -------------------
  const numItems = items.length;
  const numPacked = items.filter((item) => item.packed).length;
  const percentage = Math.round((numPacked / numItems) * 100);
-------------------------------------------------------

  return (
    <footer className='stats'>
      <em>
        {percentage === 100
          ? "You got everything! Ready to go 🛫"
          : ` 🧳 You have ${numItems} items on your list, and you already packed:
        ${numPacked} (${percentage}%)`}
      </em>
    </footer>
  );
}

```
