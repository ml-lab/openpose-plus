TAG = tensorrt:snapshot

TENSORRT_REPO_DEB = nv-tensorrt-repo-ubuntu1604-cuda9.0-ga-trt4.0.1.6-20180612_1-1_amd64.deb

tensorrt-image: $(TENSORRT_REPO_DEB)
	docker build --rm -t $(TAG) -f Dockerfile.tensorrt .

$(TENSORRT_REPO_DEB):
	cp ~/Downloads/$(TENSORRT_REPO_DEB) .

run:
	docker run --rm -it $(TAG) bash
