# Script generated with Bloom
pkgdesc="ROS - The thormang3_action_editor package This package is a action editor for thormang3. The action file which is edited by this editor will be used with this action editor."
url='http://wiki.ros.org/thormang3_action_editor'

pkgname='ros-kinetic-thormang3-action-editor'
pkgver='0.1.2_1'
pkgrel=1
arch=('any')
license=('BSD'
)

makedepends=('ncurses'
'ros-kinetic-catkin'
'ros-kinetic-robotis-controller'
'ros-kinetic-robotis-controller-msgs'
'ros-kinetic-robotis-framework-common'
'ros-kinetic-roscpp'
'ros-kinetic-std-msgs'
'ros-kinetic-thormang3-action-module'
)

depends=('ncurses'
'ros-kinetic-robotis-controller'
'ros-kinetic-robotis-controller-msgs'
'ros-kinetic-robotis-framework-common'
'ros-kinetic-roscpp'
'ros-kinetic-thormang3-action-module'
)

conflicts=()
replaces=()

_dir=thormang3_action_editor
source=()
md5sums=()

prepare() {
    cp -R $startdir/thormang3_action_editor $srcdir/thormang3_action_editor
}

build() {
  # Use ROS environment variables
  source /usr/share/ros-build-tools/clear-ros-env.sh
  [ -f /opt/ros/kinetic/setup.bash ] && source /opt/ros/kinetic/setup.bash

  # Create build directory
  [ -d ${srcdir}/build ] || mkdir ${srcdir}/build
  cd ${srcdir}/build

  # Fix Python2/Python3 conflicts
  /usr/share/ros-build-tools/fix-python-scripts.sh -v 2 ${srcdir}/${_dir}

  # Build project
  cmake ${srcdir}/${_dir} \
        -DCMAKE_BUILD_TYPE=Release \
        -DCATKIN_BUILD_BINARY_PACKAGE=ON \
        -DCMAKE_INSTALL_PREFIX=/opt/ros/kinetic \
        -DPYTHON_EXECUTABLE=/usr/bin/python2 \
        -DPYTHON_INCLUDE_DIR=/usr/include/python2.7 \
        -DPYTHON_LIBRARY=/usr/lib/libpython2.7.so \
        -DPYTHON_BASENAME=-python2.7 \
        -DSETUPTOOLS_DEB_LAYOUT=OFF
  make
}

package() {
  cd "${srcdir}/build"
  make DESTDIR="${pkgdir}/" install
}

