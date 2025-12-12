本次修改了cfg文件：
BipedCfgSF：
    command:
        curriculum = True
        lin_vel_x = [-3.0, 3.0]

    gait:
        frequencies = [1.0, 2.5]
        durations = [0.3, 0.6]
        swing_height = [0.15, 0.25]

    rewards:
        keep_balance = 2.0
        tracking_lin_vel_x = 3.0
        torques = -0.00005
        power = -1e-4

BipedPPOCfgSF：
    algorism：
        clip_param = 0.3
        entropy_coef = 0.015
        learning_rate = 5e-4  # 5.e-4
        num_learning_epochs = 6
        max_grad_norm = 1.5
    runner：
        num_steps_per_env = 32  # per iteration

为了改善上个策略不收敛的问题，降低了一点速度要求