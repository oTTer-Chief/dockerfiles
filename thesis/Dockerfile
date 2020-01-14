FROM ottr/latex

RUN apt-get update && apt-get install -y \
                python3 \
                python3-pip \
		gnuplot \
		fig2dev \
	&& rm -rf /var/lib/apt/lists/* \
        && pip3 install matplotlib numpy pandas

