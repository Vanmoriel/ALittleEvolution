# A Little Evolution
A Little Evolution is an application that through user interactions aim to reproduce the Darwin evolution of the species process.
### Idea
What the project wants to show is how one single species can evolve due to changes of environment where he lives in. 
The aim is to explain the complexity and uncontrollability of the features that characterize the process of evolution, reducing it into his simplier form using just abstract graphic. 
### Aspect
The **father** object, represented by a polygon, is located on the top part of the screen and it represent the **species that needs to evolve.** On the second row are displayed 3 polygons: they represent the **possible different evolution** that the father object can have.
Colour, size and shape are randomly defined for the species, but connected to the evolution process: each one of the represented elements will keep one of the father's characteristics, and generate two new ones. When one object is dying, it will gradually fade away. 
### Mechanism
The whole application is focused on one single species and its evolving process.
The role of the **user** will be to change the environment through his interaction, influencing the success of the three possibilities to evolve of the object. 
Giving a **life span** to objects the environment will enstablish which one is the better choice of evolution to adapt, checking which of the three possible species will be the one that can stay alive.
The last species that survive will replace the father location, becoming father itself of a new process in the evolution. 

## Interactions

The only way he can interact with species will be through:
* **Voice** - *Background HUE*
* **Shaking** - *Background Size*
* **Rotation** - *Background Brightness*

The user will control the environment that will affect the species living in with some special features:
* he will not be able to choose one single way to interact, because they'll be constantly detected.
* a "not-so-perfect" controllability of the environment.

## Used libraries

Created with the **JavaScript p5.js library** 

### Addon libraries

* p5.dom
* p5
* p5.sound

## Difficulties
### Sound
The first problem was connected with the **AudioIn function**. It does not always correcly work, so trying multiple times the issue has been detected: 
```
This uses the getUserMedia/ Stream API, which is not supported by certain
browsers.Access in Chrome browser is limited to localhost and https, but 
access over http may be limited.
```
*[AudioIn Reference](https://p5js.org/reference/#/p5.AudioIn)*

The problem was solved creating 2 applications: one useful for phones that can use the microphone and another one that use, instead of interacting by voice, the interaction by time (*where the user have to use or not his time to interact*).

### Control structures - conditionals
The hardest problem was connected to the **"if" condition**. Once all the objects where created there was the necessity to check which of them was the last living one. The following syntax works in the exposed case, but not for the other two "if". 
```
if ((thirdLp <= 0) && (secondLp <= 0)){
   //lines of code
    }
```
The problem has been fixed changing the multiple condition if with a **nested if**
```
if (secondLp <= 0){
         if (firstLp <= 0){
        }
         }
```

## Authors

Huang Liying

Giada Passerini

Runyu Tang

