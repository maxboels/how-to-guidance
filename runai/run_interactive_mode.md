# 1: runai submit to create job on dgx. Make it interactive.
runai submit test 
	-image nvcr.io/nvidia/pytorch:21.12-py3 -g 1 -p rdorent 
	--interactive 
	--host-ipc 
	--command sleep 
	--args infinity 
	-volume /nfs/home/rdorent/:/workspace/home 
	--working-dir /workspace/home

# 2: runai command to enter my image.
runai bash <image_name>

# 3: set work env. on dgx.
export HOME=/workspace/

# 4: pip3 install packages.
pip install nnunet
