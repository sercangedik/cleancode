# Clean Code
![alt tag](https://www.butterfly.com.au/images/easyblog_images/27/2e1ax_butterfly_entry_ARASH-clean-code.jpg)

##Chapter 1 - Clean Code
### The Boy Scout Rule
* Leave the campground cleaner than you found it.

### **Üstadlar için Clean Code nedir ?**

* **Bjarne Stroustrup :** Elegant and efficient.
* **Grady Booch :** Simple and direct.
* **Michael Feathers :** It looks like it was written by someone who cares.
* **Ron Jeffries :** Small, expressive, simple and no duplication.

##Chapter 2 - Meaningful Names

* Avoid disinformation
* Use pronounceable names
* Use searchable names
```java
final Popup popup = popupManager.get(stage, "/popup/friendRemovePopup.xml", true, false, 0);

float ratio = (float)game.getHeight() / (float)graphics.getHeight() ;

//rakibin chat mesaji
chatBubble = (TextBalloon) findActor("chatBubbleTop");
```
### Pick One Word per Concept
* Controller
* Manager
* Driver

![](http://s27.postimg.org/g4knt0sir/Screen_Shot_2016_01_29_at_10_37_18.png)
![](http://s30.postimg.org/v8ue5sz1d/Screen_Shot_2016_01_29_at_10_37_24.png)

### Don't pun (kelime oyunu)

* Shorter names are generally better than longer ones, so long as they are clear. Add no
more context to a name than is necessary.


##Chapter 3 - Functions

### Small !

* The first rule of functions is that they should be small. The second rule of functions is that
they should be smaller than that.

### Do One Thing

* Functions should do one thing. They should do it well. They sould do it only.

![](http://s15.postimg.org/ijk8vwnuj/Screen_Shot_2016_01_29_at_10_57_23.png)

### The Stepdown Rule
```java
 seeAMovie = ()->
     BuyTheTicket()
     watch()

 BuyTheTicket = ()->
     //some thing

 watch = () ->
     //some thing
```
### Use Descriptive Names

* Don’t be afraid to make a name long. A long descriptive name is better than a short enigmatic name.
```java
    public void logFirstTypeTwoGameTimerHandledParameter(String classDotMethod) {
		sessionLogger.append(classDotMethod + " - firstTypeTwoGameTimerHandled : " + gameModel.isFirstTypeTwoGameTimerHandled());
	}
```
### Don't Repeat Yourself !

## Chapter 4 - Comments 

### Don’t comment bad code—rewrite it.

* Formatting
* Clarification
* TODO
* Journal
* Position Markers (Okey-101 ////////////////////////)

## Chapter 5 - Formatting

* Vertical Formatting
* Horizontal Formatting (80 character standard)

![](http://s22.postimg.org/6bu8auysx/Screen_Shot_2016_01_29_at_11_03_26.png)

### Team Rules
* A team of developers should agree upon a single formatting style.

## Chapter 6 - Objects and Data Structures

### Law of Demeter 
_Talk to Friends Not to Strangers_

Function f which is inside class C can only call following functions
* Other functions of class C
* Functions of another object which is created inside f
* Functions of object which is passed as parameter to f
* Functions of another object which is an instance inside class C.

### Data Transfer Objects
* A class with public variables and no functions

### Train Wrecks
```java
Options opts = ctxt.getOptions();
File scratchDir = opts.getScratchDir();
final String outputDir = scratchDir.getAbsolutePath();


final String outputDir = ctxt.options.scratchDir.absolutePath;
```
## Chapter 7 - Error Handling

### Use Exceptions Rather Than Return Codes
* It is easy to forget
* Provide context with exceptions

### Avoid pass null && return null

## Chapter 8 - Boundaries
* Write test for the third-party code for understanding
* Abstraction

## Chapter 9 - Unit Tests

### The Three Laws of TDD
* You may not write production code until you have written a failing unit test.
* You may not write more of a unit test than is sufficient to fail, and not compiling is failing.
* You may not write more production code than is sufficient to pass the currently failing test.
 
### Tests enable the -ilities
* Flexible
* Maintainable
* Reusable

### Why ?
* If you have tests, you do not fear making changes to the code.

### Keeping test clean
* Readability
* Readability
* Readability

### One Assert per Test
* Single conclusion that is quick and easy to understand.
```java
    @Test
    public void emptyFriendsModel() {
        FriendsModel friendsModel = new FriendsModel();
        Assert.assertEquals(friendsModel.toString(), "FriendsModel [gameFriends -> 0], [installedFriends -> 0], [notInstalledFriends -> 0]");
    }
```
### Single Concept per Test
* Test a single concept in each test function.
```java
    @Test
    public void test_MatchType() {
        TournamentTableModel.MatchType matchType = TournamentTableModel.MatchType.matchTypeByRound(0);
        assertEquals(matchType, TournamentTableModel.MatchType.QUARTER_FINAL);
        assertEquals(matchType.getStage(), 1);
        matchType = TournamentTableModel.MatchType.matchTypeByRound(1);
        assertEquals(matchType, TournamentTableModel.MatchType.SEMI_FINAL);
        assertEquals(matchType.getStage(), 2);
        matchType = TournamentTableModel.MatchType.matchTypeByRound(2);
        assertEquals(matchType, TournamentTableModel.MatchType.FINAL);
        assertEquals(matchType.getStage(), 3);
        matchType = TournamentTableModel.MatchType.matchTypeByRound(1124);
        assertEquals(matchType, TournamentTableModel.MatchType.EMPTY);

        assertTrue(TournamentTableModel.MatchType.SEMI_FINAL.isBiggerThanOrEqualTo(TournamentTableModel.MatchType.QUARTER_FINAL));
        assertTrue(TournamentTableModel.MatchType.FINAL.isBiggerThanOrEqualTo(TournamentTableModel.MatchType.SEMI_FINAL));
        assertTrue(TournamentTableModel.MatchType.FINAL.isBiggerThanOrEqualTo(TournamentTableModel.MatchType.QUARTER_FINAL));
    }
```
### F.I.R.S.T.
* Fast (Tests should be fast)
* Independent (Tests should not depend on each other)
* Repeatable (Tests should be repeatable in any environment)
* Self Validating (The tests should have a boolean output)
* Timely (The tests need to be written in a timely fashion)

## Chapter 10 - Classes

* Again stepdown rule
* Classes should be small 
* The single responsibility principle (One responsibility—one reason to change)

## Chapter 11 - Systems

* Dependency Injection
* Scaling Up

## Chapter 12 - Emergence 
* Runs all the tests
* Contains no duplication
* Expresses the intent of the programmer
* Minimizes the number of classes and methods

## Chapter 13 - Smells and Heuristics
* Obsolete (Modası Geçmiş) Comment
* Poorly Written Comment
* Commented-Out Code
* No Argument is Best in Functions
* Multiple Languages in One Source File
* Code at Wrong Level of Abstraction
* Replace Magic Numbers with Named Constants
* Avoid Negative Conditionals

