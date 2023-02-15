

# 1 open new command line window connect to the server

# type hostname in terminal to get <hostname>:
    ```
    ssh -N -f -L <LOCALPORT>:<HOSTNAME>:<DGXPORT> mboels@h1
    ```

    ```
	ssh -L 11093:localhost:11093 aicheadnode
    ```

# 2.0: Activate conda env with tensorboard and tensorflow installed:
    ```
    conda activate tensorboard
    ```

# 2.1: SERVER run log file on tensorboard 
    ```
    tensorboard --logdir=/nfs/home/mboels/projects/vit-mlp-multimodal-temporal/tensorboard/<EXP>/<DATE> --port=11093
    ```