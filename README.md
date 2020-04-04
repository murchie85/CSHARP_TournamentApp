# Full C# Tournament Application.   
  

![tournamentImage](https://cdn.vox-cdn.com/thumbor/gYycEEBQahKMcA2CeglZbYjtw54=/1400x0/filters:no_upscale()/cdn.vox-cdn.com/uploads/chorus_asset/file/11519241/bracket_board.jpg)  
  
## NAVIGATION 
- [Summary](#Summary)
- [Initial Planning](#Initial-Planning)
- [DATA DESIGN](#DATA-DESIGN)
- [](#)
    
  

## Summary 
  
A tournament Tracker that sets up a schedule for teams to play each other in a single-elimination style matchups.   
Someone wants you to set up a tournament, to tell you will play who and set it up.  
  
Can be used for setting your own tournaments up such as in gaming, pingpong etc.   
Multi-form Winform application.  
SQL Database. 
Text file storage.  
Dapper.  
Linq.  
Interfaces.   
Emailing C#  
Custom Events.  
Advanced Debugging.  
  
## Initial Planning
  
It's extremely important in coding, in my experience before with COBOL development and others to flesh out the details high level design etc before getting stuck in to the app.   

**REQUIREMENTS** 
  
1. Tracks games and their outcome.  
2. Multiple competitors play.  
3. Creates a tournament plan, who plays who in what order.   
4. Schedules games.  
5. A single loss eliminates a player.  
6. The last player wins.  
  
### ASK QUESTIONS  
  
1. How many players will it handle? Is this a variable?  
2. how do we handle if the tournament doesn't have the full amount of players, can we back down to 24, 16, 8 etc.  
3. Should the ordering of who plays how be random or ordered.  
4. Should we schedule the game?   
5. If scheduled, how do we know when and how to schedule.  
6. Does system need to hold score.  
7. Where to store data?   
8. What should the front end look like?  
9. Will it handle payouts etc? 
10. What type of reporting is required?   
11. Who can fill in results? (auth)
12. Should system contact users prior to events.     

### HIGH LEVEL BIG PICTURE DESIGN  
  
**CODE** WONT be behind forms in front end.  
`STRUCTURE` Windows form   
`DATA` SQL &/OR text file.    
`USERS` One at a time on one application.    

**Key Concepts**   
  
- Email  
- SQL  
- Custom Events (how do we know to check for more games etc?)  
- Error handling.  
- Interfaces.  
- Random ordering.   
- Texting as bonus feature.  
  
## DATA DESIGN
  
 Best to do architecture design on paper or draw.io etc.  
  
**Team**   
  
- Team Members `List<person>`
- Team Name `string`  
  

**Person**  
  
- First name `string`  
- Last Name `string`    
- Email address `string`  
- Mobile number  `string`  *this isn't a number to be manipulated, so string is safer*   
   
*Break apart name early, for better use later such as in email and sorting big issues with double barrel names etc*  


