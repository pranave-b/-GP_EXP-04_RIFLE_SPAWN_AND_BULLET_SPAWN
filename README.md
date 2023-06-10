# GP_EXP-04_RIFLE_SPAWN_AND_BULLET_SPAWN
### Experiment:04 – Attach Rifle with character mesh and implementation bullet spawn from Rifle 
### AIM:
To Attach Rifle with character mesh and implementation bullet spawn from Rifle .

### ALGORITHM(for attach rifle with character mesh):
```
1.	Import the rifle asset:
•	Open your project in Unreal Engine.
•	Go to the Content Browser.
•	Right-click in the desired folder and select Import.
•	Locate and select your rifle asset file.
•	Configure the import settings as needed.
•	Click Import to bring the rifle asset into your project.
2.	Create a socket on the character mesh:
•	Open the character Blueprint that represents your character mesh.
•	In the Blueprint editor, find the Mesh component.
•	In the Details panel on the right, under the Socket section, click the "+" button to add a new socket.
•	Name the socket (e.g., "RifleSocket") and set its location and rotation relative to the character mesh.
•	Save the Blueprint.
3.	Add the rifle to the character Blueprint:
•	In the Blueprint editor, locate the Mesh component.
•	In the Details panel, under the Socket section, click the "+" button next to "Attach Children".
•	Select the rifle asset from the content browser.
•	In the Attach to field, select the Mesh component.
•	In the Socket Name field, select the socket you created in Step 2 (e.g., "RifleSocket").
•	Save the Blueprint.


4.	Adjust the rifle's position and rotation:
•	In the character Blueprint, select the rifle component.
•	In the Details panel, adjust the Transform values (location, rotation, and scale) to position and orient the rifle correctly relative to the character mesh.
•	You can also use Blueprint scripting to dynamically control the rifle's position and rotation based on the character's actions.
5.	Test the attached rifle:
•	Compile and save the character Blueprint.
•	Drag and drop the character Blueprint into the level or set it as the default character in your game mode.
•	Play the game to test the character with the attached rifle.
•	Ensure that the rifle follows the character's movements correctly.
```

OUTPUT:
GUN ATTACHED TO PLAYER
GUN ACTOR SPAWN
INPUT MAPPING
STATE GRAPH

IDLE TO GUNIDLE

GUNIDLE TO IDLE
 
GUNIDLE TO GUNRUN
 
GUNRUN TO GUNIDLE
 
INPUT ACTION TO EQUIP THE GUN
 
GUN EQUIP
 

### ALGORITHM(for implementing bullet spawn from rifle):
```
1.	Create a bullet projectile:
•	In the Content Browser, right-click in the desired folder.
•	Select Create Basic Asset > Blueprint Class.
•	In the Class Settings window, search for "Projectile" and select it as the parent class.
•	Name the Blueprint (e.g., "BulletProjectile") and click Create.
2.	Set up the bullet projectile:
•	Open the BulletProjectile Blueprint.
•	In the Blueprint editor, locate the Components panel on the left.
•	Add a Static Mesh component to represent the visual representation of the bullet.
•	Adjust the Static Mesh component's properties as desired (e.g., mesh, scale, materials, etc.).
•	Add any other necessary components (e.g., collision, audio, particle effects) to enhance the bullet's behavior.
3.	Set up the rifle Blueprint:
•	Open the rifle Blueprint that is attached to the character (refer to the previous steps on attaching the rifle).
•	In the Blueprint editor, locate the Event Graph tab.
•	Find the event that triggers the firing action (e.g., "Fire" button press).
•	Create a new custom event node for spawning the bullet projectile.
•	Drag off the custom event node and search for "Spawn Actor from Class".
•	Connect the execution line from the event node to the Spawn Actor node.
4.	Configure the Spawn Actor node:
•	In the Spawn Actor node, select the BulletProjectile Blueprint as the Class.
•	Connect the execution line from the Spawn Actor node to any necessary nodes or logic related to the firing action (e.g., setting the bullet's initial velocity, applying recoil to the rifle, playing firing sound).
5.	Adjust the spawn location and rotation:
•	Drag off the Spawn Actor node and search for "Get Socket Transform".
•	Select the character's rifle socket (the socket where the bullet should spawn).
•	Connect the output of the Get Socket Transform node to the Spawn Transform input of the Spawn Actor node.
6.	Test the bullet spawning:
•	Compile and save the rifle Blueprint and BulletProjectile Blueprint.
•	Play the game to test the character's firing action.
•	Ensure that when the firing action is triggered, the bullet projectile is spawned from the rifle's socket with the desired behavior.
```
OUTPUT:

ARROW FUNCTION
 
BULLET ACTOR 


BULLET SPAWN 
 

RESULT:
Thus, Rifle is Attached with character mesh and implementation bullet spawn from Rifle is done.


