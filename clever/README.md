API description (in Russian) for autonomous flights is available [on GitBook](https://copterexpress.gitbooks.io/clever/simple_offboard.html).

## Manual installation

Install ROS Kinetic according to the [documentation](http://wiki.ros.org/kinetic/Installation).

```bash
# Clone the repo
git clone https://github.com/CopterExpress/clever.git clever

# Build ROS packages
cd clever/catkin_ws
catkin_make -j1
```

Enable systemd service `roscore` (if not enabled):

```bash
sudo systemctl enable /home/pi/catkin_ws/src/clever/deploy/roscore.service
sudo systemctl start roscore
```

Enable systemd service `clever`:

```bash
sudo systemctl enable /home/pi/catkin_ws/src/clever/deploy/clever.service
sudo systemctl start clever
```

### Dependencies

[ROS Kinetic](http://wiki.ros.org/kinetic).

Necessary ROS packages:

* `opencv3`
* `mavros`
* `rosbridge_suite`
* `web_video_server`
* `cv_camera`
* `nodelet`
* `dynamic_reconfigure`
* `bondcpp`, branch `master`
* `roslint`
* `rosserial`
