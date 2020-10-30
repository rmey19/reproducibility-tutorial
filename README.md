


# reproducibility-tutorial
This is a repository created to discuss reproducibility for FOSS2020
    
    2  cd /scratch
    3  git clone https://github.com/rmey19/reproducibility-tutorial.git
    4  wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
    5  bash Miniconda3-latest-Linux-x86_64.sh -b -p /opt/conda
    6  ln -s /opt/conda/pkgs/*/bin/* /bin
    7  ln -s /opt/conda/pkgs/*/lib/* /usr/lib
    8  /opt/conda/bin/conda install -c conda-forge -y jupyterlab=1.2.3
    9  history >>README.md
# reproducibility-tutorial


## Computer Setup
 #download the Miniconda installer

    wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh


    # instal miniconda silently (-b) in path (-p) /opt/conda

    bash Miniconda3-latest-Linux-x86_64.sh -b -p /opt/conda


    #make sure all conda packages will be in path by symbolic links to /bin

    ln -s /opt/conda/pkgs/*/bin/* /bin

    ln -s /opt/conda/bin/* /bin

    ln -s /opt/conda/pkgs/*/lib/* /usr/lib


    # Install Jupyter lab version 1.2.3

    /opt/conda/bin/conda install -c conda-forge -y jupyterlab=1.2.3

    /opt/conda/bin/conda install -c conda-forge -y nodejs=10.13.0


    python3 -m pip install bash_kernel

    pip install ipykernel

    python3 -m bash_kernel.install


    #Test Jupyterlab

    jupyter lab --no-browser --allow-root --ip=0.0.0.0 --NotebookApp.token='' --NotebookApp.password='' --notebook-dir='/scratch/reproducibility-tutorial/'


    #Install Snakemake

    /opt/conda/bin/conda install -c bioconda -c conda-forge -y snakemake=5.8.1


    #install Docker

    # update ubuntu apt-get package manager

    sudo apt-get update


    # install some needed packages

    sudo apt-get install -y \

    apt-transport-https \

    ca-certificates \

    curl \

    gnupg-agent \

    software-properties-common


    # add the Docker key

    curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -


    #add the repository

    sudo add-apt-repository \

     "deb [arch=amd64] https://download.docker.com/linux/ubuntu \

     $(lsb_release -cs) \

     stable"


    # update apt-get with new repository information

    sudo apt-get update


    # install docker

    sudo apt-get install -y docker-ce docker-ce-cli containerd.io


    #test docker

    docker run hello-world
    1  intsP19ern
    2  cd /scratch
    3  git clone https://github.com/rmey19/reproducibility-tutorial.git
    4  wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
    5  bash Miniconda3-latest-Linux-x86_64.sh -b -p /opt/conda
    6  ln -s /opt/conda/pkgs/*/bin/* /bin
    7  ln -s /opt/conda/pkgs/*/lib/* /usr/lib
    8  /opt/conda/bin/conda install -c conda-forge -y jupyterlab=1.2.3
    9  history >>README.md
   10  nano README.md
   11  nano README.md
   12  nano README.md
   13  nano README.md
   14  nano README.md
   15  nano README.md
   16  chown -R rmey19 /scratch/reproducibility-tutorial/
   17  sudo -h
   18  scp ~/Downloads/SraRunTable.txt rmey19@123.456.78.9:/scratch/reproducibility-tutorial/
   19  scp ~/Downloads/SraRunTable.txt rmey19@128.196.142.31:/scratch/reproducibility-tutorial/
   20  clear
   21  exit
   22  mkdir /scratch/test-workflow
   23  cd /scratch/test-workflow
   24  iget -P /iplant/home/shared/cyverse_training/datasets/PRJNA79729/fastq_files/SRR064156.fastq.gz .
   25  docker run hello-world
   26  snakemake --version
   27  /opt/conda/bin/conda search -c bioconda snakemake
   28  /opt/conda/bin/conda install -c bioconda -c conda-forge -y snakemake=5.8.1
   29  ln -s /opt/conda/bin/* /bin
   30  ln -s /opt/conda/lib/* /usr/lib
   31  snakemake --version
   32  mkdir /scratch/test-workflow
   33  ls
   34  cd /scratch/test-workflow
   35  iget -P /iplant/home/shared/cyverse_training/datasets/PRJNA79729/fastq_files/SRR064156.fastq.gz .
   36  docker run -v /scratch/test-workflow/:/work quay.io/biocontainers/fastqc:0.11.7--4 fastqc /work/SRR064156.fastq.gz
   37  docker run -v /scratch/test-workflow/:/work quay.io/biocontainers/fastqc:0.11.7--4 fastqc /work/SRR064156.fastq.gz
   38  ls
   39  cd cd /scratch/test-workflow
   40  cd /scratch/test-workflow
   41  ls
   42  cd scratch
   43  cd ..
   44  ls
   45  cd rmey19
   46  mkdir scratch
   47  ls
   48  mkdir /scratch/test-workflow
   49  ls
   50  cd /scratch/test-workflow
   51  iget -P /iplant/home/shared/cyverse_training/datasets/PRJNA79729/fastq_files/SRR064156.fastq.gz .
   52  iinit
   53  iget -P /iplant/home/shared/cyverse_training/datasets/PRJNA79729/fastq_files/SRR064156.fastq.gz .
   54  docker run quay.io/biocontainers/fastqc:0.11.7--4 fastqc SRR064156.fastq.gz
   55  docker run -v /scratch/test-workflow/:/work quay.io/biocontainers/fastqc:0.11.7--4 fastqc /work/SRR064156.fastq.gz
   56  fastqc version
   57  version fastqc
   58  fastqc --version
   59  quay.io/biocontainers/trimmomatic:0.39--1
   60  docker run -v /scratch/test-workflow/:/work quay.io/biocontainers/trimmomatic:0.39--1 trimmomatic SE -threads 8 /work/SRR064156.fastq.gz /work/SRR064156_trimmed.fastq.gz SLIDINGWINDOW:4:30
   61  nano
   62  ls
   63  BashScriptForContainer
   64  rule import_from_sra:
   65    output:
   66  iget -rPV /iplant/home/shared/cyverse_training/tutorials/kallisto/03_output_kallisto_results
   67  iget -rPV /iplant/home/shared/cyverse_training/tutorials/kallisto/04_sleuth_R
   68  sudo chown -R $USER /usr/local/lib/R/site-library
   69  sudo chown -R $rmey19 /usr/local/lib/R/site-library
   70  sudo chown -R $intsP19ern /usr/local/lib/R/site-library
   71  ls
   72  head 04_sleuth_R/
   73  cd 04_sleuth_R
   74  ls
   75  cd ..
   76  docker run hello-world
   77  snakemake --version
   78  ls
   79  cd scratch
   80  sudo chown -R $USER /usr/local/lib/R/site-library
   81  ls
   82  /opt/conda/bin/jupyter lab --no-browser --allow-root --ip=0.0.0.0 --NotebookApp.token='' --NotebookApp.password='' --notebook-dir='/scratch/reproducibility-tutorial/'
   83  /opt/conda/bin/jupyter lab --no-browser --allow-root --ip=0.0.0.0 --NotebookApp.token='' --NotebookApp.password='' --notebook-dir='/scratch/reproducibility-tutorial/'conda search jupyterlab
   84  /opt/conda/bin/jupyter lab --no-browser --allow-root --ip=0.0.0.0 --NotebookApp.token='' --NotebookApp.password='' --notebook-dir='/scratch/reproducibility-tutorial/'conda search jupyterlab = 1.2.3
   85  jupyterlab --version
   86  /opt/conda/bin/conda install -c conda-forge -y jupyterlab=1.2.3
   87  /opt/conda/bin/conda install -c conda-forge -y nodejs=10.13.0
   88  /opt/conda/bin/pip install bash_kernel
   89  /opt/conda/bin/pip install ipykernel
   90  /opt/conda/bin/python3 -m bash_kernel.install
   91  conda search jupyterlab
   92  conda search jupyterlab=1.2.3
   93  /opt/conda/bin/jupyter lab --no-browser --allow-root --ip=0.0.0.0 --NotebookApp.token='' --NotebookApp.password='' --notebook-dir='/scratch/reproducibility-tutorial/'
   94  cd ..
   95  /opt/conda/bin/jupyter lab --no-browser --allow-root --ip=0.0.0.0 --NotebookApp.token='' --NotebookApp.password='' --notebook-dir='/scratch/reproducibility-tutorial/'
   96  cd /scratch
   97  git clone "https://github.com/rmey19/reproducibility-tutorial.git"
   98  /opt/conda/bin/jupyter lab --no-browser --allow-root --ip=0.0.0.0 --NotebookApp.token='' --NotebookApp.password='' --notebook-dir='/scratch/reproducibility-tutorial/'
   99  /opt/conda/bin/conda search -c bioconda snakemake
  100  /opt/conda/bin/conda install -c bioconda -c conda-forge -y snakemake=5.8.1
  101  ln -s /opt/conda/bin/* /bin
  102  ln -s /opt/conda/lib/* /usr/lib
  103  snakemake --version
  104  rstudio --version
  105  conda search RStudio
  106  sudo apt-get update
  107  sudo apt-get install -y apt-transport-https ca-certificates curl gnupg-agent software-properties-common
  108  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
  109  sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
$(lsb_release -cs) \
stable"
  110  sudo apt-get update
  111  sudo apt-get install -y docker-ce docker-ce-cli containerd.io
  112  docker run hello-world
  113  cd /scratch/reproducibility-tutorial/
  114  history >>README.md
# reprocibility tutorial

 # reproducibility-tutorial


## Computer Setup


    #download the Miniconda installer

    wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh


    # instal miniconda silently (-b) in path (-p) /opt/conda

    bash Miniconda3-latest-Linux-x86_64.sh -b -p /opt/conda


    #make sure all conda packages will be in path by symbolic links to /bin

    ln -s /opt/conda/pkgs/*/bin/* /bin

    ln -s /opt/conda/bin/* /bin

    ln -s /opt/conda/pkgs/*/lib/* /usr/lib


    # Install Jupyter lab version 1.2.3

    /opt/conda/bin/conda install -c conda-forge -y jupyterlab=1.2.3

    /opt/conda/bin/conda install -c conda-forge -y nodejs=10.13.0


    python3 -m pip install bash_kernel

    pip install ipykernel

    python3 -m bash_kernel.install


    #Test Jupyterlab

    jupyter lab --no-browser --allow-root --ip=0.0.0.0 --NotebookApp.token='' --NotebookApp.password='' --notebook-dir='/scratch/reproducibility-tutorial/'


    #Install Snakemake

    /opt/conda/bin/conda install -c bioconda -c conda-forge -y snakemake=5.8.1


    #install Docker

    # update ubuntu apt-get package manager

    sudo apt-get update


    # install some needed packages

    sudo apt-get install -y \

    apt-transport-https \

    ca-certificates \

    curl \

    gnupg-agent \

    software-properties-common


    # add the Docker key

    curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -


    #add the repository

    sudo add-apt-repository \

     "deb [arch=amd64] https://download.docker.com/linux/ubuntu \

     $(lsb_release -cs) \

     stable"


    # update apt-get with new repository information

    sudo apt-get update


    # install docker

    sudo apt-get install -y docker-ce docker-ce-cli containerd.io


    #test docker

    docker run hello-world
