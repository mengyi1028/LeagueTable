# LeagueTable
<h3>League Table</h3>
The LeagueTable class tracks the score of each player in a league. After each game, the player records their score with the recordResult function. <br/>

The player's rank in the league is calculated using the following logic:<br/>
 <ul>
  <li>The player with the highest score is ranked first (rank 1). The player with the lowest score is ranked last.</li>
   <li>If two players are tied on score, then the player who has played the fewest games is ranked higher.</li>
   <li>If two players are tied on score and number of games played, then the player who was first in the list of players is ranked higher.</li>
  </ul>
For example:<br/>
   $table = new LeagueTable(array('Mike', 'Chris', 'Arnold'));<br/>
   $table->recordResult('Mike', 2);<br/>
   $table->recordResult('Mike', 3);<br/>
   $table->recordResult('Arnold', 5);<br/>
   $table->recordResult('Chris', 5);<br/>
   echo $table->playerRank(1);<br/>
All players have the same score. However, Arnold and Chris have played fewer games than Mike, and as Chris is before Arnold in the list of players, he is ranked first. Therefore, the code above should display "Chris".<br/><br/>

[Solution](https://github.com/mengyi1028/LeagueTable/blob/main/LeagueTable.php)
