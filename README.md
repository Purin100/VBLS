Source code for VBLS paper.

This project includes 6 Python files for reproducing the VBLS model proposed in the original paper.

# VBLS
Files BLS_torch.py and BLS_class.py are source files for VBLS and vanilla BLS, respectively. The VBLS is a class named as BLS, the vanilla BLS is a class named as BLSt.

File pretrained_AID_test.py is the main source file for running VBLS and vanilla BLS related experiments.

# Stacked BLS
The source codes for Stacked BLS is copied from another GitHub project: https://github.com/MPX0222/BLS-APIs

Files BroadLearningSystem.py and StackedBroadLearningSystem.py are source files for the Stacked BLS.

Run the file test_stack.py for experiments related to Stacked BLS.

# Coding Environment
Python 3.11
PyTorch 2.4.0 with CUDA 11.8

The code may work under other versions of Python, Pytorch, and CUDA.

# Run VBLS
1. Open pretrained_AID_test.py
2. Find os.environment[CUDA_VISIBLE]. Set to "" for CPU environment.
3. Find the variables called train_path and test_path, modify them to the directory of the training set and test set, respectively.
4. Find the variable called class_num, change its value to the categories in the dataset. (AID: 30, EuroSAT: 10, NWPU-RESISC45: 45, RSSCN7: 7).
5. Find the variable called vit, set its value to vit_b_16 or vit_b_32.
6. Find variables called N1, N2 and N3. Set N2=196 for vit_b_16, or N2=49 for vit_b_32.
7. Find variable use_bls, set use_bls=True to run the VBLS model.
8. Save the pretrained_AID_test.py and open the terminal. Activate a Conda virtual environment listed in Coding Environment
9. use this command: python pretrained_AID_test.py

# Run vanilla BLS
1. Open pretrained_AID_test.py
2. Follow Step 2 to 5 in Run BLS.
3. Find variables called N1, N2 and N3. Set N1=150, N2=20, N3=2000.
4. Find variable use_bls, set use_bls=False to run the VBLS model.
5. Save the pretrained_AID_test.py and open the terminal. Activate a Conda virtual environment listed in Coding Environment
6. use this command: python pretrained_AID_test.py
