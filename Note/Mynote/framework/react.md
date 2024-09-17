


### basic functional component

```tsx
import React from 'react';

function MyComponent (){
  return (
    <div>
      <h1>Hello, World!</h1>
    </div>
  );
};

export default MyComponent;
```

### use state 
```tsx
function NameInput(){
  const [name, setName] = useState<string | null >('');  // setting the useState

  return (
            <div>
                <form>
                    <label>Enter your name:</label>
                    <input type="text" 
                            value={name} 
                            onChange={(e) => setName(e.target.value)} // Update state on change
                    />
        
                </form>
                <p>Your name is: {name}</p>
            </div>
  );
};
export default NameInput;
```


### Controlled Components
```tsx
    const [text, setText] = useState('');
    function handleSubmit(e){
        e.preventDefault(); // Prevent the default form submission
        alert(`You entered: ${text}`);
    };

    return (
        <form onSubmit={handleSubmit}>
            <input type="text"
                    value={text}
                    onChange={(e) => setText(e.target.value)}
            />
            <button type="submit">Submit</button>
        </form>
    );
```