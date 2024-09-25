# Autonomy Design Premises

### Legend
 - _ - not decided yet
 - ✔️ - accepted
 - ⏳ - accepted not essential (for future)
 - ✖️ - rejected

| Name | Description | Status |
|:---:|:---:|:---:|
| Safety | Under any circumstances rover never damages itself or anything in its environment | [_] |
| Navigability | Rover never gets stuck | [_] |
| Raw terrain | Rover is able to navigate on uneven solid and loose terrain  | [_] |
| Big obstacle size | Rover is able to traverse over obstacles up 20cm | [_] |
| Small obstacle size | Rover ignores obstacles that size is less or equal 5cm | [_] |
| Obstacle avoiding | Rover prefers to avoid any major obstacles and go around them | [_] |
| Artificial costs | System gives possibility to add not traversable artificial obstacle at runtime | [_] |
| State tracking | It is easy to get current system status | [_] |
| Stop at demand | System can be disabled at any moment remotely and it does not affects any other system | [_] |
| Reprogrammable | System can be reprogrammed (commands can be deleted and added at any time) | [_] |
| Hills and holes | Rover is able to traves though hills and holes | [_] |
| Universal | Autonomy is universal so without major changes can be adjusted and used on ARC, ARCh, URC, ERC | [_] |
| Timestamp utilization | Every message that contains timestamp has it set to correct value and receiver validates messages and do not use old data | [_] |
| Responsive | Autonomy is able to map new terrain and calculate new route in less than 5s | [_] |
| Reactive | Autonomy is able to notice new obstacles or lack of old one | [_] |
| Rover size | Autonomy in path planning takes into consideration rover size | [_] |
| One configuration source | Whole autonomy is configurable from one place | [_] |
| Multiple depth cameras | System is prepared to utilize one or more depth cameras | [_] |
| Different steering ways | System is prepared to easily change way of steering (Sliding, Ackermann, 360° turning wheels) | [_] |
| 4 submodules | Autonomy consists of 4 exchangeable and independent modules: mapper, path planner, path follower, autonomy manager | [_] |
| C++ | Whole codebase is written using C++ | [_] |
| Runs anywhere | Even if autonomy will utilize CUDA it is still compilable and runnable on device without dedicated GPU | [_] |
| Standard messages | Autonomy utilizes only standard messages - exception can be made only for communication `WebApp <=> Autonomy Manager` | [_] |
| Good practices | Whole codebase is written keeping good practices | [_] |
| Design patterns | Whole codebase is written with using design patters - with huge emphasis on `strategy` design pattern | [_] |
| Code documenting | Every function has documenting comment above it containing decryption, parameters, outputs, potential waring etc. | [_] |
| Exception handling | Every possible exception is being handled | [_] |
| No thrown exception | Code do not throw any exception ([`std::optional`](https://en.cppreference.com/w/cpp/utility/optional) or [`std::variant`](https://en.cppreference.com/w/cpp/utility/variant) - for return some additional feedback - should be used instead) | [_] |
| Easily extendable | Autonomy has quick generic and robust system to easily add new commends to it | [_] |
| Branching | Commands for autonomy manager can conditionally branch | [_] |
| One input point | Autonomy manager is the only point that takes data from WebApp and other commands about targets enabling/disabling etc. | [_] |
| One `/cmd_vel` output | The only `/cme_vel` source is autonomy manager | [_] |
| Unit Tested | Every module has unit tests | [_] |
| Tested | Whole system is tested more than once in location other than [`przed labem`](https://www.google.pl/maps/place/51%C2%B006'12.3%22N+17%C2%B005'11.8%22E/@51.103403,17.0859753,19z/data=!3m1!4b1!4m4!3m3!8m2!3d51.103403!4d17.086619?entry=ttu&g_ep=EgoyMDI0MDkyMi4wIKXMDSoASAFQAw%3D%3D) | [_] |
| Reliability | Autonomy never hardly fails - that it will require human intervention to recover or to set it up again | [_] |
| No recompilation for parameter change | Compilation is never required to change any parameter - every of them is changeable as some kind of parameters | [_] |
| Utilization of EKF | Autonomy system utilizes Extended Kalman Filter for position and rotation calculation | [_] |
| GPS | System is prepared for utilization of GPS (taking it position into consideration and navigating to certain GPS position) | [_] |
| Robot pose injection | Autonomy system gives possibility to artificially inject current robot position | [_] |
| Fused point cloud save | System is able to save fused pointcloud of viewed terrain to file | [_] |
| Map save | System is able to save current map* to file | [_] |
| Fused pointcloud to map | System is able to generate map* from provided file with fused pointcloud | [_] |
| Map load | System is able to load map* from file | [_] |

> *map - occupancy/cost/heigh map - depending on which will be used
