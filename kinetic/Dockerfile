FROM osrf/ros:kinetic-desktop-full

# For Nvidia GPU
ENV NVIDIA_VISIBLE_DEVICES ${NVIDIA_VISIBLE_DEVICES:-all}
ENV NVIDIA_DRIVER_CAPABILITIES ${NVIDIA_DRIVER_CAPABILITIES:+$NVIDIA_DRIVER_CAPABILITIES,}graphics

RUN apt-get update && apt-get install -y --no-install-recommends \
    libxext-dev libx11-dev x11proto-gl-dev dh-autoreconf\
    && rm -rf /var/lib/apt/lists/* \
    && git clone https://github.com/NVIDIA/libglvnd && cd libglvnd \\
    && ./autogen.sh && ./configure && make -j4 && make install
