本次修改了cfg文件：
BipedCfgSF：
    command:
        curriculum = True
        lin_vel_x = [-4.0, 4.0]

    gait:
        frequencies = [1.5, 2.5]
        durations = [0.3, 0.6]
        swing_height = [0.15, 0.25]

    rewards:
        keep_balance = 2.0
        tracking_lin_vel_x = 5.0
        torques = -0.00003
        power = -2e-5

BipedPPOCfgSF：
    algorism：
        clip_param = 0.3
        entropy_coef = 0.03
        num_learning_epochs = 6
        max_grad_norm = 1.5
    runner：
        num_steps_per_env = 32  # per iteration

预期效果：步频更快，速度更快，采用了curriculum策略，有助于收敛