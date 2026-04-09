# Creating a Looking Around Script

In this step, We'll create a simple C# script for using the mouse to look around. while simple, this script will have an easily modifyable sensitivity parameter, as well as clamping the rotation so players can't make the camera look inside the capsule.

1. Select your **Main Camera** and click **Add Component**.



1. Type in what you want to name your script, we'll use *mouselook*. click **New Script**, and hit enter.
    Save the script in the same place as your movement Script, and open it up in visual studio.
    You should be met with this:

    ```csharp title="mouselook.cs" linenums="1"
    using UnityEngine;

    public class mouseLooking : MonoBehaviour
    {
        // Start is called once before the first execution of Update after the MonoBehaviour is created
        void Start()
        {

        }

        // Update is called once per frame
        void Update()
        {

        }
    }
    ```
    
1. Let's set some variables.
    After `public class mouseLooking : MonoBehaviour`, add:
    ```csharp title="mouselook.cs" linenums="1"
    public class mouseLooking : MonoBehaviour
    {
        public float mouseSensitivity = 100f; //this is our sensitivity value
        public Transform playerBody; //we will assign this a value in the editor
        float xRotation = 0f; //holds the x rotation value so we can clamp it later
        ...
    }

    ```
    
    !!! warning "Variables in C#"

        Unlike Python, C# is *statically typed*. This means the datatype of the variable must be explicitly stated when declaring it. Datatypes are relatively simple, once you get the basics, but coming from Python they can be a little confusing.
        take the mouseSensitivity variable for example:

        `public float mouseSensitivity = 100f;`

        public - visibility modifier. think of this as a way of explicitly defining scope. *public* means it's accessible externally, *private* means it's not, and leaving it out implies *protected*, a pseudo-halfway point.

        float - this is the data type. this means that mouseSensitivity is a floating-point 32-bit number.

        100f - this is the value we're assigning to mouseSensitivity. the **f** explicitly tells the compiler to treat it as a float.

        Another key aspect of C# is that you always end a statement with a semicolon, hence the **;**.

        don't worry about making global variables. global variables are a rarity here, and as long as you declare your vars inside the {} after the class declaration, it's not global.

    !!! danger "forgetting the Semicolon WILL cause your code not to compile!"

1. Inside the **void Start** method, we're going to add:

    ```csharp title="mouselook.cs" linenums="1"
        // Start is called once before the first execution of Update after the MonoBehaviour is created
        void Start()
        {
            Cursor.lockState = CursorLockMode.locked;
        }
    ```
    all this will do is tell the unity project to lock your cursor to the center of the screen.

1. Go back and check your Work. press `Ctrl + S` to save your work and then tab back into Unity.
    Unity will compile your new script, and then give you a warning in the console. ignore it for now, we'll address it later. 
    You should see two extra fields that share the names of the two public methods we declared.
    Now, press on the **play** button on the top of the screen.

    ## picture of play button

    Check that your cursor does lock to the **Game** window (it will dissapear), and when confirmed, press `Esc` to free your cursor and press the stop button.

    # picture of Stop button

    !!! note "Testing"

        Testing is a critical part of game development, so test your work often.

1. heading back into VSCode, add