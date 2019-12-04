# Project report

## Algorithm
Algorithm used here is the deep deterministic policy gradient algorithm (ddpg). DDPG is a model-free policy based learning algorithm in which the agent will learn directly from the unprocessed observation spaces without knowing the domain dynamic information.


## Neural Network Architecture
### Critic
- Normalize the minibatch of states
- ReLU applied on a linear layer (256 units)
- Concatenation: add the action at the bottom of the previous output
- ReLU applied on a linear layer (128 units)
- Linear layer (output dim=1)
 
### Actor
- Normalize the minibatch of states
- ReLU applied on a linear layer (256 units)
- ReLU applied on a linear layer (128 units)
- Hyperbolic tangent applied on a linear layer (output dim=4)

## Parameters 
- Learning Rates (actor and critic): 0.001
- Replay Buffer size: int(1e6)
- Batch size: 128
- Gamma : 0.99
- Epsilon decay: 1e-6 (used to reduce the impact of the noise during the training)

## Results

<img src="https://github.com/kengying5/Continous-Control/blob/master/Images/p2-result.PNG" width="300" height="300" >

```
Episode 815 (13s)	Mean: 14.7	Moving Avg: 24.1
Episode 816 (13s)	Mean: 17.8	Moving Avg: 24.0
Episode 817 (13s)	Mean: 26.3	Moving Avg: 24.1
Episode 818 (13s)	Mean: 38.0	Moving Avg: 24.2
Episode 819 (13s)	Mean: 24.2	Moving Avg: 24.2
Episode 820 (13s)	Mean: 25.1	Moving Avg: 24.3
Episode 821 (13s)	Mean: 28.2	Moving Avg: 24.4
Episode 822 (13s)	Mean: 31.6	Moving Avg: 24.5
Episode 823 (13s)	Mean: 31.1	Moving Avg: 24.5
Episode 824 (13s)	Mean: 28.9	Moving Avg: 24.5
Episode 825 (13s)	Mean: 27.4	Moving Avg: 24.5
Episode 826 (13s)	Mean: 26.2	Moving Avg: 24.7
Episode 827 (13s)	Mean: 25.8	Moving Avg: 24.6
Episode 828 (13s)	Mean: 26.6	Moving Avg: 24.6
Episode 829 (13s)	Mean: 27.2	Moving Avg: 24.7
Episode 830 (13s)	Mean: 23.9	Moving Avg: 24.8
Episode 831 (13s)	Mean: 27.9	Moving Avg: 24.8
Episode 832 (13s)	Mean: 29.5	Moving Avg: 24.9
Episode 833 (12s)	Mean: 32.3	Moving Avg: 24.9
Episode 834 (13s)	Mean: 29.7	Moving Avg: 24.9
Episode 835 (13s)	Mean: 26.8	Moving Avg: 25.0
Episode 836 (13s)	Mean: 19.0	Moving Avg: 24.9
Episode 837 (13s)	Mean: 27.8	Moving Avg: 24.9
Episode 838 (13s)	Mean: 33.7	Moving Avg: 25.0
Episode 839 (12s)	Mean: 31.6	Moving Avg: 25.1
Episode 840 (12s)	Mean: 29.0	Moving Avg: 25.2
Episode 841 (12s)	Mean: 15.0	Moving Avg: 25.1
Episode 842 (13s)	Mean: 34.5	Moving Avg: 25.2
Episode 843 (13s)	Mean: 30.5	Moving Avg: 25.3
Episode 844 (13s)	Mean: 23.7	Moving Avg: 25.3
Episode 845 (13s)	Mean: 31.7	Moving Avg: 25.3
Episode 846 (12s)	Mean: 32.7	Moving Avg: 25.3
Episode 847 (12s)	Mean: 29.7	Moving Avg: 25.4
Episode 848 (13s)	Mean: 30.3	Moving Avg: 25.5
Episode 849 (13s)	Mean: 22.9	Moving Avg: 25.5
Episode 850 (13s)	Mean: 30.4	Moving Avg: 25.6
Episode 851 (12s)	Mean: 34.0	Moving Avg: 25.7
Episode 852 (12s)	Mean: 32.8	Moving Avg: 25.8
Episode 853 (12s)	Mean: 18.0	Moving Avg: 25.7
Episode 854 (12s)	Mean: 29.5	Moving Avg: 25.7
Episode 855 (13s)	Mean: 25.3	Moving Avg: 25.7
Episode 856 (13s)	Mean: 33.3	Moving Avg: 25.7
Episode 857 (13s)	Mean: 25.4	Moving Avg: 25.7
Episode 858 (12s)	Mean: 26.1	Moving Avg: 25.7
Episode 859 (13s)	Mean: 28.4	Moving Avg: 25.8
Episode 860 (13s)	Mean: 32.3	Moving Avg: 25.9
Episode 861 (13s)	Mean: 25.0	Moving Avg: 25.9
Episode 862 (13s)	Mean: 29.7	Moving Avg: 26.0
Episode 863 (13s)	Mean: 33.0	Moving Avg: 26.2
Episode 864 (13s)	Mean: 24.9	Moving Avg: 26.2
Episode 865 (13s)	Mean: 29.2	Moving Avg: 26.2
Episode 866 (13s)	Mean: 32.6	Moving Avg: 26.3
Episode 867 (13s)	Mean: 19.5	Moving Avg: 26.2
Episode 868 (13s)	Mean: 35.6	Moving Avg: 26.3
Episode 869 (13s)	Mean: 34.6	Moving Avg: 26.3
Episode 870 (13s)	Mean: 32.0	Moving Avg: 26.4
Episode 871 (13s)	Mean: 27.2	Moving Avg: 26.5
Episode 872 (13s)	Mean: 30.3	Moving Avg: 26.6
Episode 873 (13s)	Mean: 26.6	Moving Avg: 26.7
Episode 874 (13s)	Mean: 31.6	Moving Avg: 26.7
Episode 875 (13s)	Mean: 33.2	Moving Avg: 26.8
Episode 876 (13s)	Mean: 20.9	Moving Avg: 26.7
Episode 877 (13s)	Mean: 27.4	Moving Avg: 26.8
Episode 878 (13s)	Mean: 38.7	Moving Avg: 26.9
Episode 879 (13s)	Mean: 33.8	Moving Avg: 27.0
Episode 880 (13s)	Mean: 35.3	Moving Avg: 27.1
Episode 881 (13s)	Mean: 29.1	Moving Avg: 27.3
Episode 882 (13s)	Mean: 28.3	Moving Avg: 27.2
Episode 883 (13s)	Mean: 33.4	Moving Avg: 27.3
Episode 884 (13s)	Mean: 29.0	Moving Avg: 27.3
Episode 885 (13s)	Mean: 35.4	Moving Avg: 27.4
Episode 886 (13s)	Mean: 31.7	Moving Avg: 27.5
Episode 887 (13s)	Mean: 35.3	Moving Avg: 27.5
Episode 888 (13s)	Mean: 27.8	Moving Avg: 27.6
Episode 889 (13s)	Mean: 31.3	Moving Avg: 27.7
Episode 890 (13s)	Mean: 36.0	Moving Avg: 27.8
Episode 891 (13s)	Mean: 31.2	Moving Avg: 27.9
Episode 892 (13s)	Mean: 29.1	Moving Avg: 28.0
Episode 893 (13s)	Mean: 26.4	Moving Avg: 28.0
Episode 894 (13s)	Mean: 24.9	Moving Avg: 28.0
Episode 895 (13s)	Mean: 32.0	Moving Avg: 28.1
Episode 896 (13s)	Mean: 35.0	Moving Avg: 28.2
Episode 897 (14s)	Mean: 30.2	Moving Avg: 28.3
Episode 898 (13s)	Mean: 25.2	Moving Avg: 28.4
Episode 899 (13s)	Mean: 31.8	Moving Avg: 28.5
Episode 900 (13s)	Mean: 27.8	Moving Avg: 28.5
Episode 901 (13s)	Mean: 30.9	Moving Avg: 28.6
Episode 902 (13s)	Mean: 37.8	Moving Avg: 28.8
Episode 903 (13s)	Mean: 29.1	Moving Avg: 28.8
Episode 904 (13s)	Mean: 36.6	Moving Avg: 28.9
Episode 905 (13s)	Mean: 20.7	Moving Avg: 28.8
Episode 906 (13s)	Mean: 27.9	Moving Avg: 28.8
Episode 907 (13s)	Mean: 28.9	Moving Avg: 28.8
Episode 908 (13s)	Mean: 26.1	Moving Avg: 28.8
Episode 909 (13s)	Mean: 31.7	Moving Avg: 28.8
Episode 910 (13s)	Mean: 32.5	Moving Avg: 28.9
Episode 911 (13s)	Mean: 33.8	Moving Avg: 29.0
Episode 912 (13s)	Mean: 22.7	Moving Avg: 29.0
Episode 913 (13s)	Mean: 33.8	Moving Avg: 29.1
Episode 914 (13s)	Mean: 34.5	Moving Avg: 29.2
Episode 915 (13s)	Mean: 34.9	Moving Avg: 29.4
Episode 916 (13s)	Mean: 29.5	Moving Avg: 29.5
Episode 917 (13s)	Mean: 25.1	Moving Avg: 29.5
Episode 918 (13s)	Mean: 35.9	Moving Avg: 29.4
Episode 919 (13s)	Mean: 29.8	Moving Avg: 29.5
Episode 920 (14s)	Mean: 26.4	Moving Avg: 29.5
Episode 921 (13s)	Mean: 35.8	Moving Avg: 29.6
Episode 922 (13s)	Mean: 37.5	Moving Avg: 29.7
Episode 923 (13s)	Mean: 34.6	Moving Avg: 29.7
Episode 924 (13s)	Mean: 33.3	Moving Avg: 29.7
Episode 925 (13s)	Mean: 33.8	Moving Avg: 29.8
Episode 926 (13s)	Mean: 35.5	Moving Avg: 29.9
Episode 927 (13s)	Mean: 33.8	Moving Avg: 30.0
Episode 928 (13s)	Mean: 33.9	Moving Avg: 30.0

Environment solved in 828 episodes!	Average Score: 30.04
```

## Ideas for future works
 1. Add more noise to the network itself
 2. To tune the model better with hyperparameters
 3. Implement a prioritized replayed-buffer 
