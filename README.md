# Miami Traffic Prediciton and Evacuation

#### Contributors:
- Stephen Tse
- Marguerite Siboni
- Kevin Roesch
- Eli Regen

### Problems Statement:

In the event of a natural disaster capable of causing massive property damage and loss, evacuating people to areas of safety becomes the top priority. Miami, Florida is a city that is routinely plagued by hurricanes, with Hurricane Florence occurring less than a year ago. While modern GPS is practical and effictive it fails on two fronts during a disaster. Firstly, many systems don't use real-time data to update their maps. For day to day predictions this isn't much of a problem as rush hour occurs at about the same time everyday, but when sudden changes in road conditions can have an enormous difference in people's livelihoods a constantly updating evacution plan is needed.

By leveraging social media, specifically twitter, we hope to model road closures and complications as they happen and create a plan for the Florida government to act on in case of emergency; one that can adjust as needed to changing situations.

### Data Collection

Due to limitations in the Twitter API, only allowing for tweets from a one week timeframe to be gathered, we used a package called GetOldTweets3 which allowed us to gather tweets from select news and traffic reporting twitter pages over the past year. An alternative appraoch that we undertook was collecting as many tweets as possible over the one week allowed window, regardless of source, and tried using those as well. The first method produced more usable observations, whereas the second produced more information per observation.

The second method proved to be more reliable and as the traffic data was more recent we were able to determine road closures easily so in the end we focused on the one week prior to data collection when modeling.

### Modeling

Multiple models we tested, but the Random Forest Tree Classifier proved to be the most effective though occasionally overfit. Test set accuracy for each row was cosistently above the baseline

### Application

As mentioned previously, the intention of this project is to optimize evacution strategy. The model itself already has applications in optimizing routing, say from a starting point to a destination, but when a large population is try to move in the same general direction something more complex is required to prevent even more traffic problems from arising. 

