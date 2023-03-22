# startup
This repository is for CS260. It is for assignments only. The project repo can be found here: github.com/Watermeloncl/startup-breadwinner. The Project itself can be found here: bread-winner.click.

#### GitHub Assignment, due 1/25.
So far, this repository is entirely practice for using GitHub.  For this assignment, I learned how to better merge conflicts in VS Code. I feel like I have a better understanding of how my IDE interacts with GitHub.

#### Simon-HTML Assignment, due 2/8
Linking different files  

```
<tag><a href="index.html">Home</a></tag>  
```

Useful for navigating to different pages  

Using SVG:
(M move <to x,y>, Q quadratic curve <control point x,y> <to x,y>)  

```
<path d="M 95,5 95,95 5,95 Q 5,5 95,5" fill="green" />  
```

Removing from accessibility searches  
aria-hidden="true"  

#### Simon-CSS Assignment, due 2/21
Linking CSS in

```
<link rel="stylesheet" href="main.css" />
```

Adding Bootstrap

```
<link
      href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.2/dist/css/bootstrap.min.css"
      rel="stylesheet"
      integrity="sha384-Zenh87qX5JnK2Jl0vWa8Ck2rdkQ2Bzep5IDxbcnCeuOxjzrPF/et3URy9Bv1WTRi"
      crossorigin="anonymous"
    />
```

Options:
flex-direction: row | row-reverse | column | column-reverse  
align-items: center | stretch | flex-start | flex-end | baseline  
justify-content: normal | flex-end | flex-start | space-between | space-around  
Learning more about flex: <a href="https://flexboxfroggy.com/">Home</a>  
Learning more about grid: <a href="https://cssgridgarden.com/">Home</a>  

#### Simon-JavaScript Assignment, due 3/6
Adding JavaScript in (consider putting it at the end if it references HTML during initialization to avoid collision and something being accessed before initialization)  

```
<script src="play.js"></script>
```

Math.floor always rounds down  
Math.round rounds regularly  

localStorage can be accessed anywhere using setItem or getItem  
Use unique ID's when storing in localStorage to avoid overwriting previous data  

splice() inserts into an array, using splice(index, [numOfEntriesToDelete], [newValue], [...otherNewValues])  
JSON.parse() to turn from JSON to String  
JSON.stringify() to turn from String to JSON  

creating a date as a String according to local time can be done through new Date().toLocaleDateString()  

Great ForEach loop  
for(const [index, value] of structure.entries())   (structure is name of the array or other)  


#### JavaScript Deliverable
timerVariable = setInterval(function, milliseconds)  
clearInterval(timerVariable)  
  
document.querySelector("#id").textContent DOESN'T call document parser  
pause intervals for intense computationally expensive calculations  
arrayName.length = 0 to empty array  
  
const elementName = document.createElement("elementType"); to create element  
elementName.className = classNameToChangeTo  
elementName.id = idNameToChangeTo  
  
for (const [i, item] of Items.entries()), i for index, item for actual value (or object), Items for structure  
No pass by reference! (No explicit pointers :( Unless you wrap in an object and parse before using.)  
Use more global constants and more functions with parameters next time instead of global variables (good thing it's single threaded, huh? Oh wait no it's super slow haha)  
  
#### Simon Service  
app.listen is the equivelant of linux command listen()  
Fetching json:  
  
```  
const response = await fetch('/api/scores');  
scores = await response.json();  
```  
  
Router:  
  
```  
var apiRouter = express.Router();  
app.use(`/api`, apiRouter);  
```  
  
Get:  
  
```  
apiRouter.get('/scores', (_req, res) => {  
  res.send(scores);  
});  
```  
  
Post:  
  
```  
apiRouter.post('/score', (req, res) => {  
  scores = updateScores(req.body, scores);  
  res.send(scores);  
});  
```  
