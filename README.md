# Learning-Journal-GP
Learning Journal for Games Programming (Year 2)

15/10/24
- Created learning journal
- Getting to understand the process of learning code
- Learnt that coding scripts is a step by step build up process.

22/10/24
Planning and Brainstorming Ideas for my tutorials:
- First Person movement and jumping in a 3d Environment.
- Taking damage i.e. from high ground, from objects like Spikes
- Meter bar for things like HP


- Started the First Person Movement, first starting with using a random game object (capsule) and tested its horizontal movement.
- Searched through tutorials and had a go at them. Bumped into many issues such as misunderstanding certain scripts and objects in Unity.
- The main reason for this was because the tutorial had skipped major parts i.e. didnt show the process of creating emptyobjects, cameras etc.
- It also referenced to other tutorials they had created, so it wasn't exactly successful when working on the movement. So instead, I looked for a new tutorial and that was successful.
- As I was planning, I realised that those should be done after I do other steps, i.e. taking damage means I'd have to make a health system. So I took a step back, and decided a HP system should be completed first.

29/10/24
- Continued with First Person POV movement, searched for other tutorials.
- Decided to work on First Person POV first and was successful, little to no issues/errors.
- Began working on movement
- First started with the Camera, created a script solely for the Camera, the camera being in first person POV and it is controlled simply by moving the mouse.
- I attached the main camera, that is created from simply creating a Unity project, to my Player and the first person POV was successful, as well as the camera movement.
- Went back to work on player movement, and it was somewhat confusing and bumped into a lot of issues since I wasn't able to understand what was going on, so I restarted and searched for a different tutorial.
- The main reason for it, was because the tutorial I was looking at, had skipped a few major steps, like creating the empty objects and making more than 1 camera, so I was unsure of what to do, and couldn't figure it out.
- I looked for a different tutorial, and this tutorial was a lot better at explaining, and included the major parts when explaining how things works and what to add.
- Movement became a lot more successful, with little to no issues. It contains simple movement with jumping, and has a lookXLimit so it doesnt look further than say 90 degrees.

05/11/2024
- Finalised the player Movement, and began to work on the Health System.
- I found a tutorial on a health system that functions like Dark Souls, and used the tutorial to help on the health system.
- I bumped into a small issue where, one of the HP bars, which functions as the main HP, to not actually appear in the scene.
- What I did was, rearrange some of th objects and emptyobjects in the inspector, connecting so that it becomes a parent/child.
- I had had to re-shape the hp bar since I found out that, duplicating an object, doesn't fully copy everything and that was what went wrong, so once I fixed the shape of the main HP Bar, it displayed in the scene and works
how it should do.
- I went to the object that has the shape of the HP bar, and I had to re-shape the Anchor preset in the Rect Transform component, once I did that for the duplicated object, it appeared this time when I tested it and functioned how it should.

12/11/2024
- Last week I finished the health system, and now this week, it's about my player taking damage.
- I'll be experimenting i.e. taking damage from other objects (these objects will be playing as enemies/environmental objects i.e. spikes)
- I began searching for a tutorial online.

15/11/2024
- Started to work on tutorial 3, where my player takes damage when coming into contact with something, in this case it'll be a placeholder object (a cube)
- I managed to find a tutorial on how to get these objects to damage my player when coming into contact, I bumped into a few issues when working on this tutorial.
- What went wrong was that whenever my character came into contact with the object, I wasn't being damaged or losing HP.
- I thought it was an issue with the script, but it turns out I forgot to add in components to the cube playholder, rigidbody.
- Once I added the rigidbody, I actually started to take damage when coming into contact with the cube.

19/11/2024
- Continuing the taking damage tutorial work.
- Bumping into issues where taking damage is inconsistent.
- I'm using a cube as a placeholder and whenever I bump into it, I either take damage, or I don't which isn't supposed to happen. I'm supposed to take damage whenever I come into contact with the cube.

26/11/2024
- Began my last tutorial, which is the Menu System.
- A lot of tutorials involve a main menu system where it includes backgrounds, but I didn't have one so I had to look for one that did not contain a background.
- I went with a tutorial that included a background, but I was able to skip the background step, and focus on the buttons for the Menu system.
- I then found one and started the tutorial. I bumped into an issue where my text wasn't appearing when I created a buttion - Text Mesh Pro, but then I figured out that I had to install the Text Mesh Pro imports and then the text appeared for my button.
- For the most part, the tutorial went smoothly and didn't bump into issues for majority of the way through, but towards the end, I bumped into 2 issues.
- One of which, was that my "back" and "quit" button were overlapping initially, but whenever I clicked some of the buttons, it resolved the issue, but never resolved the initial start.
- I solved it simply hiding then "back" button, and it fixed the overlapping issue, whilst still appearing when it needs needed.
- The second issue was that whenever I clicked the "play", it did not load my tutorial scene.
- I solved the issue, which was the "SceneManager.LoadScene" line was actually incorrect, so I changed it so that it tags the Tutorial scene and once I clicked "Play" again, it loaded into the Tutorial scene and worked.
- After I finish with the Menu system tutorial, I got back to tutorial 3, which is the tutorial where you take damage when colliding with an object.
- The issue I faced was that the damage I take when colliding with an object was really inconsistent. Sometimes I collide with an object, I take damage but sometimes I don't.
- Eventually it got to the point where I asked for help, and we noticed that whenever I take damage, it's when the object I'm colliding with, moves.
- Whenever I bumped into it, sometimes it would get knocked over and that's when I take damage.
- So what I ended up doing was, removing "OnCollisionEnter" part in my PlayerCollision script, and instead changed to an "OnTriggerEnter" command.
- I then adjusted the radius for my Players' Capsule Collider, as well as the Obstacles' Box Collider, and once I tested it again, the damage was a lot more consistent and what I wanted.
- I now take damage every single time I make contact with the object. 


