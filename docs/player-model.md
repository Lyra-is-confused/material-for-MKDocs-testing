```js title="code-examples.md" linenums="1" hl_lines="2-4"
// Function to concatenate two strings
function concatenateStrings(str1, str2) {
  return str1 + str2;
}

// Example usage
const result = concatenateStrings("Hello, ", "World!");
console.log("The concatenated string is:", result);
```

# Creating a Player model  

Before you start, you need to create a project for your game. A player model can be something as simple as a bean, or something as complex as realistic human-like creatures(change sentence). For this part of the tutorial, we will only be creating a simple "bean" player model.

To create your player model, hover over the **GameObject** option on the top-bar, hover over the **3D Object** tab, then select **Capsule**. We select capsule, because it's the best basic player model according to the internet.

<figure markdown="span">
  ![Player Creation](player1.png){ width="700" height="700" }
  
<figcaption>Your player model will show up on the highlighted Hierarchy</figcaption>
</figure>

Alternatively, you can right-click on the Hierarchy, and follow the same steps as listed above.  

<figure markdown="span">
  ![Player Creation2](alt.png){ width="700" height="700" }
  
<figcaption>Both options are fine</figcaption>
</figure>