#Compare scripts in two directories.
Set up vimdiffext plugin.
diff dir1 dir2 | vim -R - at shell.

#Visualize network structure on remote machine
	local machine: ssh -L 6006:127.0.0.1:6006 server@ip
		ssh -L 6006:127.0.0.1:6006 xliu167@remote_ip

	remote machine: tensorboard --logdir <path> --port 6006
	navigate to http://localhost:6006 on the local machine

#Separate .json with newlines
	jq . ./results/CornerNet/None/test/results.json > ./result.json

#Access tot jupyter
jupyter notebook \
  --NotebookApp.allow_origin='https://colab.research.google.com' \
  --port=8888 \
  --NotebookApp.port_retries=0

#Grep keywords with line-numbers
grep -i -n "Keywords" <filename>


#To remove the last commit from git, you can simply run 
	git reset --hard HEAD^ 
#If you are removing multiple commits from the top, you can run 
	git reset --hard HEAD~2 
#to remove the last two commits.

#Add large files
1.git lfs install

#Activate TensorFlow on M1 Mac
conda activate mlp
jupyter notebook

#Adding large files to Github
git lfs track "*.h5"
git lfs push --all origin main
git add .
git commit -am "add large file"
git push -u origin main
