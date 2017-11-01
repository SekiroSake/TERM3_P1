# How does path planning work
### How to make it run
Before I could make a plan planing, first off, let the car run, regardless of the traffic and safety;)
```
            double dist_inc = 0.5;
            for(int i =0; i < 50; i++){
                next_x_vals.push_back(car_x + (dist_inc * i)*cos(deg2rad(car_yaw)));
                next_y_vals.push_back(car_y + (dist_inc * i)*sin(deg2rad(car_yaw)));
            }
```
This code simply push the next 50 dots with sequentially every .02 seconds into next x and y value stack which could let the car start to run.
![](https://github.com/hang-wang/TERM3_P1/blob/master/image/run.gif)

After then vehicle could move, we need to have the vehicle stay in the lane.
Set the constant lane so far.
```$xslt
 double next_d = 6;
```

Here frenet is helpful for providing the necessary next x vals and y vals into the next val array
getXY function transforms  Frenet s,d coordinates to Cartesian x,y.

now push the new points into the next_val array
```$xslt
next_x_vals.push_back(xy[0]);
next_y_vals.push_back(xy[1]);
```
Now the vehicle could run following the lane.
![](https://github.com/hang-wang/TERM3_P1/blob/master/image/run2.gif)
![](https://github.com/hang-wang/TERM3_P1/blob/master/image/run3.gif)
![](https://github.com/hang-wang/TERM3_P1/blob/master/image/run4.gif)
![](https://github.com/hang-wang/TERM3_P1/blob/master/image/run5.gif)
