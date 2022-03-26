# Minesweeper Applications
As a part of my CST-227 Enterprise Applications Programming II course, I developed a fully functional Minesweeper game in C#. This project went through several iterations as I progressed through the course. 

As part of this project, I created a backend Minesweeper library that I could implement into multiple project in order to easily create different versions of minesweeper. For the first phase of this project, I developed the backend library while hooking it up to a console application on the frontend. 
<p align="center">
  <img width="400" src="https://user-images.githubusercontent.com/101227901/160229317-81db4746-be6d-4569-a79e-bc485cd0d894.png" alt="Console Version of the Minesweeper Game">
  <br>
  <i>Console Version of the Minesweeper Game</i>
</p>


I created two main objects in the Minesweeper library, the Cell object and the Board object. These objects worked on the backend to create a gameboard, populate it with cells, let the user reveal a cell to be clear or a bomb, let the user flag a cell, and end the game in victory or defeat.
```csharp
//===================================//
//==========Class=Variables==========//
//===================================//
//Cells position in column and row
public int cellRow { get; set; } = -1;
public int cellColumn { get; set; } = -1;

//If the cell is a mine, replacement for "live" value
public Boolean isMine { get; set; }

//Is this cell flagged by the player
public Boolean isFlagged { get; set; } = false;

//If the cell has been checked by the player, replacement for "visited" value
public Boolean hasBeenChecked { get; set; } = false;

//How many mines are touching this cell, replacement for the neighboring "live" cells
public int numberOfMinesTouching { get; set; } = 0;
```
<p align="center">
<i>Cell Object's Class Variables in the Minesweeper Library</i>
</p>


In Minesweeper, if a player clicks on a non-bomb cell, the game will then clear all non-bomb cells in every direction, until it hits a non-bomb cell that is touching a bomb. This feature is also known as flood fill. I worked to build a flood fill system that used recursive logic that revealed non-bomb cells to a player. This system required a lot of fine-tuning, to perfect, as this was my first serious dive into the topic of recursion and it took me a little bit to fully grasp the concept. As a wise man once said, "To understand recursion, you must know recursion."
```csharp
//==============================//
//==========Flood=Fill==========//
//==============================//
private void floodFill(int r, int c)
{
	boardGrid[r, c].hasBeenChecked = true;  //Saying it has been checked

	if (boardGrid[r, c].numberOfMinesTouching == 0)
	{
		//Northern Check
		if (isValid(r + 1, c) == true &&
		boardGrid[r + 1, c].isMine == false &&
		boardGrid[r + 1, c].hasBeenChecked == false)
		{
			floodFill(r + 1, c);
		}
		...
	}
}
```
<p align="center">
  <i>The Flood Fill Method in the Board Object Class that Recursively Revealed all Cells that were not Bombs</i>
</p>

After developing the main functions of the Minesweeper Library, I then worked to implement it into a Windows Form Application. This allowed me to drastically improve the user experience with the game, as now the user could easily click buttons instead of typing out commands to a command console. 

<p align="center">
  <img width="400" src="https://user-images.githubusercontent.com/101227901/160229678-da920641-fe39-4a15-83b8-4fd02772309a.png" alt="Windows Form Version of the Minesweeper Game">
  <br>
  <i>Windows Form Version of the Minesweeper Game</i>
</p>

The implementation of the Minesweeper library into Windows Forms was interesting, as I needed to create a frontend button that was attached to the backend Minesweeper Cell Object being used to run the game.
```csharp
//====Creating=Board====//
gameBoard = new Board(futureBoardSize, futureBoardDifficulty);  //Instantiating new board

//====Creating=Board=View====//
buttonGrid = new Button[futureBoardSize, futureBoardSize];  //Instantiating a new button grid
```
<p align="center">
  <i>Creating a Board Object and a Button Grid Object to Mirror it</i>
</p>


An extra feature I added onto the windows application was the addition of score tracking. This allowed users to enter in their username, play a game, and then have their score recorded. I also built the score viewer so that players could see the scores for different difficulties and board sizes.
<p align="center">
  <img width="400" src="https://user-images.githubusercontent.com/101227901/160229752-8d8ad8a1-94a4-46ae-bbcb-88a94fbba460.png" alt="Cataloged Scores of Board Size of 1 and Difficulty of 1">
  <br>
  <i>Cataloged Scores of Board Size of 1 and Difficulty of 1</i>
</p>
