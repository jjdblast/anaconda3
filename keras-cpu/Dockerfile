FROM okwrtdsh/anaconda3:tf-cpu

RUN apt-get update -qq \
 && apt-get install --no-install-recommends -y \
	# keras.utils.vis_utils
	graphviz \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*

# keras (tensorflow) install
RUN conda install -y --quiet \
	'keras=2.2.0' \
 && pip --no-cache-dir install \
	# keras.utils.vis_utils
	pydot_ng
