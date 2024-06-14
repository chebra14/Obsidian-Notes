## Follow the Gap for Obstacle Avoidance

 Follow the gap is an obstacle avoidance algorithm

- Without a map?
- The LiDAR senses creates a vector range of how far away an object is 
- -eg. [0.5, 5.1 ,6, 7, inf, 3, inf, 3, inf, 8, 1, 3]
- inf means that there are no obstacles in front
- For the middle inf, has a close by object so it might not be a good choice.
- Definition of a gap: Series of n consecutive hits that pass at some distance t
- Follow the centre of the widest available gap in the range

- **Find the gaps**
- **Calculate the width of each gap**
- **Determine the widest gap**
- **Optimal: Determine the "deepest" gap**

- Doesn't work for non-holomic robot in an environment with dense obstacles.
- If 2 positions not blocked by an obstacle, but the robot needs to reposition to reach that goal.

- Follow the gap doesn't account for the car hitting the edges. Decide a distance threshold for small maneuvers
- Estimate the obstacle and car as a circle that fully encapsulates the footprint 

- **Find the nearest LIDAR point and put a "safety bubble" around it of radius rb**
- **Set all points inside the bubble to distance 0. All nonzero points are considered 'free space.'**
- **Find maximum length sequence of consecutive non-zeros among the 'free space' points - The max-gap**
- **Find the 'best' point among this maximum length sequence. Choose furthest point in free space, and set your steering angle towards it.**

- Every update creates 'skittsh' behaviour. If the obstacle is far away, smoothly curve into the gap over the distance. 
- Find disparity in the LIDAR (large gaps between numbers).
- For each disparity, extend it half the width of the car.
- Choose a path based on virtual LIDAR readings.

- Cornering
- When turning, the car mustn't hit an obstacle.
- If the obstacle on the side of the car mustn't be coming towards the car.
- Scan all available LIDAR samples below -90 or above +90 degrees. These will cover the sides of the car to the track.
- If any point is below a safe distance on the side of the car in the direction the car is turning, stop turning, just keep going straight.
- Fails when the car is very close to the inside, and the track is wide.

- Minimise wiggle
- The robot set their direction to the deepest range.
- Can set a threshold, and travel to the centre point of the deepest gap.