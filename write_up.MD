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
