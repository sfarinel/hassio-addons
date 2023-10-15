FROM quantumentangledandy/neolink:latest

RUN apt-get update && \
    apt-get install -y \
        jq \
        libgstrtspserver-1.0-0 \
        libgstreamer1.0-0 \
        libgstreamer-plugins-bad1.0-0 \
        gstreamer1.0-x \
        gstreamer1.0-plugins-base \
        gstreamer1.0-plugins-good \
        gstreamer1.0-plugins-bad && \

    apt-get clean -y && rm -rf /var/lib/apt/lists/*

  
# Copy data for add-on
COPY run.sh /
RUN chmod a+x /run.sh

CMD [ "/run.sh" ]
