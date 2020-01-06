# Source code

If you want to access the OPEN source code, follow this link: https://github.com/Ivsucram/ATL_Matlab

# Reference

[ArXiv -> ATL: Autonomous Knowledge Transfer from Many Streaming Processes](https://arxiv.org/abs/1910.03434)

[ResearchGate -> ATL: Autonomous Knowledge Transfer from Many Streaming Processes](https://www.researchgate.net/publication/336361712_ATL_Autonomous_Knowledge_Transfer_from_Many_Streaming_Processes)

# ATL
ATL: Autonomous Knowledge Transfer from Many Streaming Processes

1. Clone ATL git do your computer, or just download the files.

2. Provide a dataset by replacing the file `data.csv`

	Right now, data.csv here has SEA dataset data. You can open and check by yourself.
	
	`data.csv` must be prepared as following:
  
		- Each row presents a new data sample
		- Each column presents a data feature
		- The last column presents the label for that sample. Don't use one-hot encoding.

3. Open Matlab. The code was developed using Matlab 2018b, so if you use an older version, you might get some error.

	You can use Matlab 2018b or newer.
	
	Matlab may prompt you to install some official add-ons, as:
  
		- Deep Learning Toolbox
		- Fuzzy Logic Toolbox
		- Digital Processing Signal Toolbox

4. Inside Matlab, travel until the folder where you downloaded ATL.

5. On the Matlab terminal, just type "ATL". This will execute ATL, which will read your data.csv and process it.

	ATL will automatically normalize your data and split your data into 2 streams (Source and Target data streams), with a bias between them.

	Matlab will print ATL status at the end of every minibatch, where you will be able to follow useful information as:
  
		- Training time (maximum, mean, minimum, current and accumulated)
		- Testing time (maximu, mean, minimum, current and accumulated)
		- The number of GMM clusters (maximum, mean, minimum and current)
		- The Target Classification rate
		- And a quick review of ATL structure (both discriminative and generative phases), where you can see how many automatically generated nodes were created

	At the end of the process, Matlab will plot 6 graphs:
  
		- Network bias and Network variance w.r.t. the generative phase
		- Network bias and Network variance w.r.t. the discriminative phase
		- The Target and Source Classificarion Rate evolution, as well as the final mean accuracy of the network, for both Source and Target
		- All losses over time, and how they influence the network learning
		- The evolution of GMMs on Source and Target AGMM over time
		- The processing time per mini-batch and as well as the total processing time, both for training and testing

Thank you.

# Download all datasets used on the paper

As some datasets are too big, we can't upload them to GitHub. GitHub as a size limit of 35MB per file. Because of that, you can find all the datasets in a csv format on the anonymous link below.
To test it, copy the desired dataset to the same folder as ATL and rename it to "data.csv".

- https://drive.google.com/drive/folders/1Te0KMqJ5DUVuJK3tVt1l3AbHuKR4CxP9 
