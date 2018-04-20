# Script generated with Bloom
pkgdesc="ROS - The offset_tuner_server package"
url='http://wiki.ros.org/thormang3_offset_tuner_server'

pkgname='ros-kinetic-thormang3-offset-tuner-server'
pkgver='0.1.2_1'
pkgrel=1
arch=('any')
license=('BSD'
)

makedepends=('ros-kinetic-catkin'
'ros-kinetic-cmake-modules'
'ros-kinetic-robotis-controller'
'ros-kinetic-robotis-controller-msgs'
'ros-kinetic-roscpp'
'ros-kinetic-std-msgs'
'ros-kinetic-thormang3-base-module'
'ros-kinetic-thormang3-offset-tuner-msgs'
)

depends=('ros-kinetic-cmake-modules'
'ros-kinetic-roscpp'
'ros-kinetic-std-msgs'
)

conflicts=()
replaces=()

_dir=thormang3_offset_tuner_server
source=()
md5sums=()

prepare() {
    cp -R $startdir/thormang3_offset_tuner_server $srcdir/thormang3_offset_tuner_server
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

