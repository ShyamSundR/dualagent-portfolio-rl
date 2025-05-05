{\rtf1\ansi\ansicpg1252\cocoartf2822
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\froman\fcharset0 Times-Bold;\f1\froman\fcharset0 Times-Roman;\f2\fmodern\fcharset0 Courier-Bold;
\f3\fmodern\fcharset0 Courier;\f4\froman\fcharset0 TimesNewRomanPSMT;}
{\colortbl;\red255\green255\blue255;\red0\green0\blue0;\red0\green0\blue0;}
{\*\expandedcolortbl;;\cssrgb\c0\c0\c0;\cssrgb\c0\c1\c1;}
{\*\listtable{\list\listtemplateid1\listhybrid{\listlevel\levelnfc23\levelnfcn23\leveljc0\leveljcn0\levelfollow0\levelstartat1\levelspace360\levelindent0{\*\levelmarker \{disc\}}{\leveltext\leveltemplateid1\'01\uc0\u8226 ;}{\levelnumbers;}\fi-360\li720\lin720 }{\listname ;}\listid1}
{\list\listtemplateid2\listhybrid{\listlevel\levelnfc0\levelnfcn0\leveljc0\leveljcn0\levelfollow0\levelstartat1\levelspace360\levelindent0{\*\levelmarker \{decimal\}}{\leveltext\leveltemplateid101\'01\'00;}{\levelnumbers\'01;}\fi-360\li720\lin720 }{\listlevel\levelnfc23\levelnfcn23\leveljc0\leveljcn0\levelfollow0\levelstartat1\levelspace360\levelindent0{\*\levelmarker \{circle\}}{\leveltext\leveltemplateid102\'01\uc0\u9702 ;}{\levelnumbers;}\fi-360\li1440\lin1440 }{\listname ;}\listid2}
{\list\listtemplateid3\listhybrid{\listlevel\levelnfc0\levelnfcn0\leveljc0\leveljcn0\levelfollow0\levelstartat1\levelspace360\levelindent0{\*\levelmarker \{decimal\}}{\leveltext\leveltemplateid201\'01\'00;}{\levelnumbers\'01;}\fi-360\li720\lin720 }{\listlevel\levelnfc23\levelnfcn23\leveljc0\leveljcn0\levelfollow0\levelstartat1\levelspace360\levelindent0{\*\levelmarker \{circle\}}{\leveltext\leveltemplateid202\'01\uc0\u9702 ;}{\levelnumbers;}\fi-360\li1440\lin1440 }{\listname ;}\listid3}}
{\*\listoverridetable{\listoverride\listid1\listoverridecount0\ls1}{\listoverride\listid2\listoverridecount0\ls2}{\listoverride\listid3\listoverridecount0\ls3}}
\margl1440\margr1440\vieww11520\viewh8400\viewkind0
\deftab720
\pard\pardeftab720\sa280\partightenfactor0

\f0\b\fs28 \cf0 \expnd0\expndtw0\kerning0
## Dual-agent reinforcement learning (RL)
\f1\b0\fs24 \
The dual-agent reinforcement learning (RL) architecture used in this project is intended to optimize portfolios across S&P 500 stocks and cryptocurrencies (BTC, ETH). The structure is made up of:\
\pard\pardeftab720\partightenfactor0
\cf0 The PPO-based strategic agent maximizes long-term risk-adjusted returns.\
A DQN-based tactical agent that takes advantage of transient volatility patterns\
\
Through a differentiable auction mechanism, the agents work together to enable dynamic risk budgeting in response to changing market regimes. Cross-market correlation modeling, market regime detection with HMMs, and thorough feature engineering are all included in the project.
\fs28 \
\pard\pardeftab720\sa280\partightenfactor0
\cf0 \
\pard\pardeftab720\sa280\partightenfactor0

\f0\b \cf0 \
## Files\
\pard\tx220\tx720\pardeftab720\li720\fi-720\sa240\partightenfactor0
\ls1\ilvl0
\f2\fs26 \cf0 \kerning1\expnd0\expndtw0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
Datapreprocess.ipynb
\f1\b0\fs24 \uc0\u8232 Complete data preprocessing pipeline. Downloads historical market data (S&P 500, BTC, ETH), calculates rolling features (returns, volatility, correlation), detects market regimes using HMM, and saves the aligned dataset in Parquet format. Also generates visualizations for EDA.\
\ls1\ilvl0
\f2\b\fs26 \kerning1\expnd0\expndtw0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
SinglePPO.ipynb
\f1\b0\fs24 \uc0\u8232 Implements a single-agent PPO baseline model \
\ls1\ilvl0
\f2\b\fs26 \kerning1\expnd0\expndtw0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
DualAgentFinal.ipynb
\f1\b0\fs24 \uc0\u8232 Main training notebook that implements the proposed dual-agent reinforcement learning\
\pard\pardeftab720\sa280\partightenfactor0

\f0\b\fs28 \cf0 \
\
## How to Run\
\pard\tx220\tx720\pardeftab720\li720\fi-720\sa240\partightenfactor0
\ls2\ilvl0
\fs24 \cf0 \kerning1\expnd0\expndtw0 {\listtext	1	}\expnd0\expndtw0\kerning0
Step 1
\f1\b0 : Run 
\f3\fs26 SignlePPO.ipynb
\f1\fs24 \
\pard\tx940\tx1440\pardeftab720\li1440\fi-1440\sa240\partightenfactor0
\ls2\ilvl1\cf0 \kerning1\expnd0\expndtw0 {\listtext	
\f4 \uc0\u9702 
\f1 	}\expnd0\expndtw0\kerning0
Trains the Single gent model with top 10 stocks \
\ls2\ilvl1\kerning1\expnd0\expndtw0 {\listtext	
\f4 \uc0\u9702 
\f1 	}\expnd0\expndtw0\kerning0
Produces exploratory figures in 
\f3\fs26 figures/\
\ls2\ilvl1
\f1\fs24 \kerning1\expnd0\expndtw0 {\listtext	
\f4 \uc0\u9702 
\f1 	}Also produces model files in results_dir/\expnd0\expndtw0\kerning0
\
\pard\tx220\tx720\pardeftab720\li720\fi-720\sa240\partightenfactor0
\ls2\ilvl0
\f0\b \cf0 \kerning1\expnd0\expndtw0 {\listtext	2	}\expnd0\expndtw0\kerning0
Step 2
\f1\b0 : Open and execute 
\f3\fs26 Datapreprocess.ipynb
\f1\fs24 \
\pard\tx940\tx1440\pardeftab720\li1440\fi-1440\sa240\partightenfactor0
\ls2\ilvl1\cf0 \kerning1\expnd0\expndtw0 {\listtext	
\f4 \uc0\u9702 
\f1 	}\expnd0\expndtw0\kerning0
Loads data from finance\
\ls2\ilvl1\kerning1\expnd0\expndtw0 {\listtext	
\f4 \uc0\u9702 
\f1 	}\expnd0\expndtw0\kerning0
Handles Nan values and produces clean_data.csv\
\ls2\ilvl1\kerning1\expnd0\expndtw0 {\listtext	
\f4 \uc0\u9702 
\f1 	}\expnd0\expndtw0\kerning0
Also produces exploratory figures\
\pard\tx220\tx720\pardeftab720\li720\fi-720\sa240\partightenfactor0
\ls2\ilvl0
\f0\b \cf0 \kerning1\expnd0\expndtw0 {\listtext	3	}\expnd0\expndtw0\kerning0
Step 3: 
\f1\b0 Open and execute 
\f3\fs26 DualagentFinal.ipynb\
\pard\pardeftab720\sa240\partightenfactor0
\ls3\ilvl1
\f1\fs24 \cf0 \kerning1\expnd0\expndtw0 {\listtext	
\f4 \uc0\u9702 
\f1 	}\expnd0\expndtw0\kerning0
Loads preprocessed data\
\ls3\ilvl1\kerning1\expnd0\expndtw0 {\listtext	
\f4 \uc0\u9702 
\f1 	}\expnd0\expndtw0\kerning0
Generates 
\f3\fs26 enhanced features data/enhanced_features.csv
\f1\fs24 \
\ls3\ilvl1\kerning1\expnd0\expndtw0 {\listtext	
\f4 \uc0\u9702 
\f1 	}\expnd0\expndtw0\kerning0
Trains dual-agent system\
\ls3\ilvl1\kerning1\expnd0\expndtw0 {\listtext	
\f4 \uc0\u9702 
\f1 	}\expnd0\expndtw0\kerning0
Applies differentiable auction mechanism\
\ls3\ilvl1\kerning1\expnd0\expndtw0 {\listtext	
\f4 \uc0\u9702 
\f1 	}\expnd0\expndtw0\kerning0
Evaluates on test periods using custom backtesting logic\
\ls3\ilvl1\kerning1\expnd0\expndtw0 {\listtext	
\f4 \uc0\u9702 
\f1 	}Produces Portfolio asset allocation plots \
{\listtext	
\f4 \uc0\u9702 
\f1 	}Also produces portfolio performance plots\expnd0\expndtw0\kerning0
\
\pard\pardeftab720\sa240\partightenfactor0
\cf0 \
\
## Below is a list of relevant trained model outputs and their approximate sizes:\

\itap1\trowd \taflags0 \trgaph108\trleft-108 \trbrdrt\brdrnil \trbrdrl\brdrnil \trbrdrr\brdrnil 
\clvertalc \clshdrawnil \clwWidth4056\clftsWidth3 \clmart10 \clmarl10 \clmarb10 \clmarr10 \clbrdrt\brdrnil \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt20 \clpadl20 \clpadb20 \clpadr20 \gaph\cellx2880
\clvertalc \clshdrawnil \clwWidth4872\clftsWidth3 \clmart10 \clmarl10 \clmarb10 \clmarr10 \clbrdrt\brdrnil \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt20 \clpadl20 \clpadb20 \clpadr20 \gaph\cellx5760
\clvertalc \clshdrawnil \clwWidth1315\clftsWidth3 \clmart10 \clmarl10 \clmarb10 \clmarr10 \clbrdrt\brdrnil \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt20 \clpadl20 \clpadb20 \clpadr20 \gaph\cellx8640
\pard\intbl\itap1\pardeftab720\sl264\slmult1\qc\partightenfactor0

\f0\b \cf3 File Name\cell 
\pard\intbl\itap1\pardeftab720\sl264\slmult1\qc\partightenfactor0
\cf3 Description\cell 
\pard\intbl\itap1\pardeftab720\sl264\slmult1\qc\partightenfactor0
\cf3 Approx. Size\cell \row

\itap1\trowd \taflags0 \trgaph108\trleft-108 \trbrdrl\brdrnil \trbrdrr\brdrnil 
\clvertalc \clshdrawnil \clwWidth4056\clftsWidth3 \clmart10 \clmarl10 \clmarb10 \clmarr10 \clbrdrt\brdrnil \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt20 \clpadl20 \clpadb20 \clpadr20 \gaph\cellx2880
\clvertalc \clshdrawnil \clwWidth4872\clftsWidth3 \clmart10 \clmarl10 \clmarb10 \clmarr10 \clbrdrt\brdrnil \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt20 \clpadl20 \clpadb20 \clpadr20 \gaph\cellx5760
\clvertalc \clshdrawnil \clwWidth1315\clftsWidth3 \clmart10 \clmarl10 \clmarb10 \clmarr10 \clbrdrt\brdrnil \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt20 \clpadl20 \clpadb20 \clpadr20 \gaph\cellx8640
\pard\intbl\itap1\pardeftab720\sl264\slmult1\partightenfactor0

\f3\b0\fs26 \cf3 ppo_single_agent.zip
\f1\fs24 \cell 
\pard\intbl\itap1\pardeftab720\sl264\slmult1\partightenfactor0
\cf3 Trained PPO model for single-agent baseline\cell 
\pard\intbl\itap1\pardeftab720\sl264\slmult1\partightenfactor0
\cf3 ~240kb\cell \row

\itap1\trowd \taflags0 \trgaph108\trleft-108 \trbrdrl\brdrnil \trbrdrt\brdrnil \trbrdrr\brdrnil 
\clvertalc \clshdrawnil \clwWidth4056\clftsWidth3 \clmart10 \clmarl10 \clmarb10 \clmarr10 \clbrdrt\brdrnil \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt20 \clpadl20 \clpadb20 \clpadr20 \gaph\cellx2880
\clvertalc \clshdrawnil \clwWidth4872\clftsWidth3 \clmart10 \clmarl10 \clmarb10 \clmarr10 \clbrdrt\brdrnil \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt20 \clpadl20 \clpadb20 \clpadr20 \gaph\cellx5760
\clvertalc \clshdrawnil \clwWidth1315\clftsWidth3 \clmart10 \clmarl10 \clmarb10 \clmarr10 \clbrdrt\brdrnil \clbrdrl\brdrnil \clbrdrb\brdrnil \clbrdrr\brdrnil \clpadt20 \clpadl20 \clpadb20 \clpadr20 \gaph\cellx8640
\pard\intbl\itap1\pardeftab720\sl264\slmult1\partightenfactor0

\f3\fs26 \cf3 rolling_window_results.pkl
\f1\fs24 \cell 
\pard\intbl\itap1\pardeftab720\sl264\slmult1\partightenfactor0
\cf3 Serialized backtest results over evaluation window\cell 
\pard\intbl\itap1\pardeftab720\sl264\slmult1\partightenfactor0
\cf3 ~700kb\cf0 \cell \lastrow\row
}