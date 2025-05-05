## Dual-agent reinforcement learning (RL)

The dual-agent reinforcement learning (RL) architecture used in this project is intended to optimize portfolios across S&P 500 stocks and cryptocurrencies (BTC, ETH). The structure is made up of:
The PPO-based strategic agent maximizes long-term risk-adjusted returns.
A DQN-based tactical agent that takes advantage of transient volatility patterns

Through a differentiable auction mechanism, the agents work together to enable dynamic risk budgeting in response to changing market regimes. Cross-market correlation modeling, market regime detection with HMMs, and thorough feature engineering are all included in the project.


## Files
	•	Datapreprocess.ipynb Complete data preprocessing pipeline. Downloads historical market data (S&P 500, BTC, ETH), calculates rolling features (returns, volatility, correlation), detects market regimes using HMM, and saves the aligned dataset in Parquet format. Also generates visualizations for EDA.
 	•	Risk Parity.ipynb Implements riskparity one of the baselines
	•	SinglePPO.ipynb Implements a single-agent PPO baseline model 
	•	DualAgentFinal.ipynb Main training notebook that implements the proposed dual-agent reinforcement learning


## How to Run
	1	Step 1: Run SignlePPO.ipynb
		◦	Trains the Single gent model with top 10 stocks 
		◦	Produces exploratory figures in figures/
		◦	Also produces model files in results_dir/
	2	Step 2: Open and execute Datapreprocess.ipynb
		◦	Loads data from finance
		◦	Handles Nan values and produces clean_data.csv
		◦	Also produces exploratory figures
	3	Step 3: Open and execute DualagentFinal.ipynb
		◦	Loads preprocessed data
		◦	Generates enhanced features data/enhanced_features.csv
		◦	Trains dual-agent system
		◦	Applies differentiable auction mechanism
		◦	Evaluates on test periods using custom backtesting logic
		◦	Produces Portfolio asset allocation plots 
		◦	Also produces portfolio performance plots


## Below is a list of relevant trained model outputs and their approximate sizes:

- ppo_single_agent.zip  
  Trained PPO model for single-agent baseline ~240kb
- rolling_window_results.pkl
  Serialized backtest results over evaluation window ~700kb
