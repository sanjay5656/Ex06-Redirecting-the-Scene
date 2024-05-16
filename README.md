
# Ex06-Redirecting-the-Scene

## Aim:
To Redirecting the scene in the unity engine.

## Algorithm:
Step 1:
To open the unity engine.

Step 2:
Create a new 3D project.

Step 3:
Create plane and name it as ground and create cube and name it as player.

Step 4:
Add WinText in Hierarchy.

Step 5:
Create a C# Script and name it as playercontroller and add the script to player.

Step 6:
Use the R button to change the level2

Step 7
Print the Output and end the program.

## Program:

```c#
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.SceneManagement;


public class PlayerController : MonoBehaviour
{
    Rigidbody rb;
    public GameObject WinTXT;
    void Start()
    {
        rb=GetComponent<Rigidbody>();
    }
    void Update()
    {
        if (Input.GetKeyDown(KeyCode.W))
        {
            SceneManager.LoadScene("Level2");
        }
    }
    private void OnCollisionEnter(Collision Other)
    {
        if (Other.gameObject.tag=="Destroy")
        {
            Destroy(Other.gameObject);
            WinTXT.SetActive(true);
        }
    }
}
```

## Output:
#### Mini Game
![Screenshot 2024-05-16 181045](https://github.com/sanjay5656/Ex06-Redirecting-the-Scene/assets/115128955/337efb9c-3e68-4f7b-8f46-2f59aca4a33b)


![Screenshot 2024-05-16 181147](https://github.com/sanjay5656/Ex06-Redirecting-the-Scene/assets/115128955/bbd27aab-b0b6-49cf-9152-43da52562b38)


## Result:

The above C# coding is successfully redirecting the scene in the unity engine.
