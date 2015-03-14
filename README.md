# wdi-pre-work_march2015
Pre-work for WDI Hong Kong March 2015

// ROCK PAPER SCISSORS HOMEWORK 


////////////////////////////////////////////////
/*   Provided Code - Please Don't Edit   */
////////////////////////////////////////////////
'use strict';

function getInput() {
    console.log("Please choose either 'rock', 'paper', or 'scissors'.")
    return prompt();
}
function randomPlay() {
    var randomNumber = Math.random();
    if (randomNumber < 0.33) {
        return "rock";
    } else if (randomNumber < 0.66) {
        return "paper";
    } else {
        return "scissors";
    }
}
////////////////////////////////////////////////
/*           Write Your Code Below            */
////////////////////////////////////////////////

/* function getPlayerMove(move) {
    // Write an expression that operates on a variable called `move`
    // If a `move` has a value, your expression should evaluate to that value.
    // However, if `move` is not specified / is null, your expression should equal `getInput()`.
    return /* Your Expression */

/* function getComputerMove(move) {
    // Write an expression that operates on a variable called `move`
    // If a `move` has a value, your expression should evaluate to that value.
    // However, if `move` is not specified / is null, your expression should equal `randomPlay()`.
    return /* Your Expression */

function getPlayerMove(move) {
    var move;
    if (move != null) {
    move = move;
  } else {
    move = getInput();
  }
}

function getComputerMove(move) {
    var move;
    if (move != null) { 
    move = move;
    } else {
    move = randomPlayer();
    }
}


    // Write code that will set winner to either 'player', 'computer', or 'tie' based on the values of playerMove and computerMove.
    // Assume that the only values playerMove and computerMove can have are 'rock', 'paper', and 'scissors'.
    // The rules of the game are that 'rock' beats 'scissors', 'scissors' beats 'paper', and 'paper' beats 'rock'.
    /* YOUR CODE HERE */
    if(playerMove == "rock" && computerMove == "paper"){
        winner = "computer"
        console.log("Computer wins!");
    }
    else if(playerMove == "paper" && computerMove == "rock"){
        winner = "player"
        console.log("Player wins!");
    }
    else if(playerMove == "paper" && computerMove == "scissors"){
        winner = "computer"
        console.log("Computer wins!");
    }
    else if(playerMove == "scissors" && computerMove == "paper"){
        winner = "player"
        console.log("Player wins!");
    }
    else if(playerMove == "scissors" && computerMove == "rock"){
        winner = "computer"
        console.log("Computer wins!");
    }
    else if(playerMove == "rock" && computerMove == "scissors"){
        winner = "player"
        console.log("Player wins!");
    }
    else{
        winner = "tie"
        console.log("It's a tie!");
    }
    
    return winner;
}

function playToFive() {
    console.log("Let's play Rock, Paper, Scissors");
    var playerWins = 0;
    var computerWins = 0;
    
    // Write code that plays 'Rock, Paper, Scissors' until either the player or the computer has won five times.
    /* YOUR CODE HERE */
    
   while (playerWins < 5 && computerWins < 5) {   
        var getWinnerMove = getPlayerMove(); 
        var getComputerMove = getComputerMove();
   }
    
        if (winner === "player") {
        playerWins++;
        console.log("playerWins");
        }
        else if (winner === "computer") {
        computerWins++;
        console.log("computerWins");
        }
        else {
        playerWins++ && computerWins++;
        console.log("tie");
        }
        console.log("You chose " + playerMove + ". " + "The computer chose " + computerMove + ".");
        console.log(winner);
        console.log("The score so far is " + playerWins + " : " + computerWins + ".");

   }
   
    return [playerWins, computerWins];

playToFive();
