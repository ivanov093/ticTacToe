ticTacToe
=========
import javax.swing.JOptionPane;
import java.lang.Math;

public class ticTacToe
{
  public static void main( String[] args)
  {
  	// Variables
  	int compMove;
  	int userMove;
  	int turn = ( ( (int)(Math.random()*2) ) + 1 );
  	int gamesWon = 0;
  	int gamesLost = 0;
  	int gamesPlayed = 0;
  	int gamesTied = 0;
  	String winnerPrompt= "";
  	String errorPrompt = "You can't make that move. Try again";
  	String again;
  	String winnerResult;
  	boolean madeMove;
  	
  	// 1 Game
  	do
  	{
  		boolean winner = false;
  		
  		// to evaluate when game ends and a tie must have been reached:
  		int numberOfTotalMoves = 0; 
  		gamesPlayed += 1;
  		
  		//place holders:
  		String a = "1";
  		String b = "2";
  		String c = "3";
  		String d = "4";
  		String e = "5";
  		String f = "6";
  		String g = "7";
  		String h = "8";
  		String i = "9";
  		
  		// Game frame
  		String gameBoard = String.format( 
  				"%s|%s|%s\n%s|%s|%s\n%s|%s|%s", a, b, c, d, e, f, g, h, i);
  		JOptionPane.showMessageDialog(null, gameBoard);
  		
  		
  		do
  		{
  			gameBoard = String.format( 
  				"%s|%s|%s\n%s|%s|%s\n%s|%s|%s", a, b, c, d, e, f, g, h, i);
  				
  				
  			// 1.1.1 Move Assignments
  			
  			// 1.1.1.1 Computer Turn
  			if( turn % 2 == 0)
  			{
  				do
  				{
  					// 1.1.1.1.2 Precise Computer Move
  					compMove = ( (int)(Math.random()*9 + 1) );
  					madeMove = true;
  					
  					// 1.1.1.1.2 Position of Computer Move in framework
  					switch (compMove)
  					{
  						case 1: 
  							if ( a != "x" && a != "o")
  							{
  								a = "x";
  								numberOfTotalMoves += 1;
  							}
  							else
  							{
  								madeMove = false;
  							}
  							break;
  						case 2: 
  							if ( b != "x" && b != "o")
  							{
  								b = "x";
  								numberOfTotalMoves += 1;
  							}
  							else
  							{
  								madeMove = false;
  							}
  							break;
  						case 3: 
  							if ( c != "x" && c != "o")
  							{
  								c = "x";
  								numberOfTotalMoves += 1;
  							}
  							else
  							{
  								madeMove = false;
  							}
  							break;
  						case 4: 
  							if ( d != "x" && d != "o")
  							{
  								d = "x";
  								numberOfTotalMoves += 1;
  							}
  							else
  							{
  								madeMove = false;
  							}
  							break;
  						case 5: 
  							if ( e != "x" && e != "o")
  							{
  								e = "x";
  								numberOfTotalMoves += 1;
  							}
  							else
  							{
  								madeMove = false;
  							}
  							break;
  						case 6: 
  							if ( f != "x" && f != "o")
  							{
  								f = "x";
  								numberOfTotalMoves += 1;
  							}
  							else
  							{
  								madeMove = false;
  							}
  							break;
  						case 7: 
  							if ( g != "x" && g != "o")
  							{
  								g = "x";
  								numberOfTotalMoves += 1;
  							}
  							else
  							{
  								madeMove = false;
  							}
  							break;
  						case 8: 
  							if ( h  != "x" && h != "o")
  							{
  								h = "x";
  								numberOfTotalMoves += 1;
  							}
  							else
  							{
  								madeMove = false;
  							}
  							break;
  						case 9: 
  							if ( i  != "x" && i != "o")
  							{
  								i = "x";
  								numberOfTotalMoves += 1;
  							}
  							else
  							{
  								madeMove = false;
  							}
  							break;
  					}
  				}
  				while(!madeMove);
  			}
  			
  			// 1.1.1.2 User Turn
  			else
  			{
  				do
  				{
  					// 1.1.1.2.1 User Move
  					userMove = Integer.parseInt( 
  						JOptionPane.showInputDialog( 
  						"Make your move (1-9)\n" + gameBoard ));
  					madeMove = true;
  					
  					// 1.1.1.2.2 Poition of User Move in framework
  					switch (userMove)
  					{
  						case 1: 
  							if ( a != "x" && a!= "o")
  							{
  								a = "o";
  								numberOfTotalMoves += 1;
  							}
  							else
  							{
  								JOptionPane.showMessageDialog(null, errorPrompt);
  								madeMove = false;
  							}
  							break;
  						case 2: 
  							if ( b != "x" && b != "o")
  							{
  								b = "o";
  								numberOfTotalMoves += 1;
  							}
  							else
  							{
  								JOptionPane.showMessageDialog(null, errorPrompt);
  								madeMove = false;
  							}
  							break;
  						case 3: 
  							if ( c != "x" && c != "o")
  							{
  								c = "o";
  								numberOfTotalMoves += 1;
  							}
  							else
  							{
  								JOptionPane.showMessageDialog(null, errorPrompt);
  								madeMove = false;
  							}
  							break;
  						case 4: 
  							if ( d != "x" && d != "o")
  							{
  								d = "o";
  								numberOfTotalMoves += 1;
  							}
  							else
  							{
  								JOptionPane.showMessageDialog(null, errorPrompt);
  								madeMove = false;
  							}
  							break;
  						case 5: 
  							if ( e != "x" && e != "o")
  							{
  								e = "o";
  								numberOfTotalMoves += 1;
  							}
  							else
  							{
  								JOptionPane.showMessageDialog(null, errorPrompt);
  								madeMove = false;
  							}
  							break;
  						case 6: 
  							if ( f != "x" && f != "o")
  							{
  								f = "o";
  								numberOfTotalMoves += 1;
  							}
  							else
  							{
  								JOptionPane.showMessageDialog(null, errorPrompt);
  								madeMove = false;
  							}
  							break;
  						case 7: 
  							if ( g != "x" && g != "o")
  							{
  								g = "o";
  								numberOfTotalMoves += 1;
  							}
  							else
  							{
  								JOptionPane.showMessageDialog(null, errorPrompt);
  								madeMove = false;
  							}
  							break;
  						case 8: 
  							if ( h != "x" && h != "o")
  							{
  								h = "o";
  								numberOfTotalMoves += 1;
  							}
  							else
  							{
  								JOptionPane.showMessageDialog(null, errorPrompt);
  								madeMove = false;
  							}
  							break;
  						case 9: 
  							if ( i != "x" && i != "o")
  							{
  								i = "o";
  								numberOfTotalMoves += 1;
  							}
  							else
  							{
  								JOptionPane.showMessageDialog(null, errorPrompt);
  								madeMove = false;
  							}
  							break;
  					}
  				}
  				while(!madeMove);
  			}
  			
  			// used to evaluate whether player or computer turn
  			turn += 1;
  			
  			// 1.1.1.3 determine winner
  			if (a == b && b == c)
  			{
  				if( a == "x")
  				{
  					winnerPrompt = "computer wins!!";
  					gamesLost += 1;
  				}
  				else if( a == "o")
  				{
  					winnerPrompt = "player wins!!";
  					gamesWon += 1;
  				}
  				winner = true;
  			}
  			else if (a == d && d == g)
  			{
  				if( a == "x")
  				{
  					winnerPrompt = "computer wins!!";
  					gamesLost += 1;
  				}
  				else if( a == "o")
  				{
  					winnerPrompt = "player wins!!";
  					gamesWon += 1;
  				}
  				winner = true;
  			}
  			else if (a == e && e == i)
  			{
  				if( a == "x")
  				{
  					winnerPrompt = "computer wins!!";
  					gamesLost += 1;
  				}
  				else if( a == "o")
  				{
  					winnerPrompt = "player wins!!";
  					gamesWon += 1;
  				}
  				winner = true;
  			}
  			else if (c == f && f == i)
  			{
  				if( c == "x")
  				{
  					winnerPrompt = "computer wins!!";
  					gamesLost += 1;
  				}
  				else if( c == "o")
  				{
  					winnerPrompt = "player wins!!";
  					gamesWon += 1;
  				}
  				winner = true;
  			}
  			else if (c == e && e == g)
  			{
  				if( c == "x")
  				{
  					winnerPrompt = "computer wins!!";
  					gamesLost += 1;
  				}
  				else if( c == "o")
  				{
  					winnerPrompt = "player wins!!";
  					gamesWon += 1;
  				}
  				winner = true;
  			}
  			else if (e == b && b == h)
  			{
  				if( e == "x")
  				{
  					winnerPrompt = "computer wins!!";
  					gamesLost += 1;
  				}
  				else if( e == "o")
  				{
  					winnerPrompt = "player wins!!";
  					gamesWon += 1;
  				}
  				winner = true;
  			}
  			else if (e == d && d == f)
  			{
  				if( e == "x")
  				{
  					winnerPrompt = "computer wins!!";
  					gamesLost += 1;
  				}
  				else if( e == "o")
  				{
  					winnerPrompt = "player wins!!";
  					gamesWon += 1;
  				}
  				winner = true;
  			}
  			else if (g == h && h == i)
  			{
  				if( g == "x")
  				{
  					winnerPrompt = "computer wins!!";
  					gamesLost += 1;
  				}
  				else if( g == "o")
  				{
  					winnerPrompt = "player wins!!";
  					gamesWon += 1;
  				}
  				winner = true;
  			}
  			else if (numberOfTotalMoves == 9)
  			{
  				winnerPrompt = "We tied...";
  				gamesTied += 1;
  				winner = true;
  			}
  		}
  		while(!winner);
  		
  		// 1.1.2 Single game results
  		
  		// Game framework after game
  		JOptionPane.showMessageDialog(null,String.format( 
  			"%s|%s|%s\n%s|%s|%s\n%s|%s|%s", a, b, c, d, e, f, g, h, i));
  		// Winner Announcement
  		JOptionPane.showMessageDialog(null, winnerPrompt);
  	
  	
  		// 2.3 Ask if play again
  		again = 
  		JOptionPane.showInputDialog( "Do you want to play again?"
  			+ "\nEnter y for yes\n or any other key to end game." );
  	}
  	while(again.equalsIgnoreCase("Y"));
  	
  	
  	
  	// 2 Results
  	
  	int percentWon = ((gamesWon * 100) / gamesPlayed);
  	int percentLost = ((gamesLost * 100) / gamesPlayed);
  	String gamesWonPrompt = "Games User Won: " + gamesWon;
  	String gamesLostPrompt = "\nGames Computer Won: " + gamesLost;
  	String gamesTiedPrompt = "\nGames Tied: " + gamesTied;
  	String gamesPlayedPrompt = "\nGames Played: " + gamesPlayed;
  	String percentWonPrompt = "\nPercentage User Won: " + percentWon + "%";
  	String percentLostPrompt = "\nPercentage Computer Won: " + percentLost + "%";
  	
  	if (gamesWon > gamesLost)
  	{
  		winnerResult = "\nYou Won Overall!!!";
  	}
  	else
  	{
  		winnerResult = "\nYou Lost Overall...";
  	}
  	
  	JOptionPane.showMessageDialog(null, gamesWonPrompt + gamesLostPrompt +
  		gamesPlayedPrompt + percentWonPrompt + percentLostPrompt + winnerResult );
  }
}
