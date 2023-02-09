# cGAN-colorization-NN-project

Original paper https://arxiv.org/abs/1611.07004

Shrek is love, Shrek is life

⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢀⣀⠀⠀⠀⠀⠀⠀⠀⠀⢀⡴⠖⠛⠉⠉⠉⠙⠲⢄⡀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢠⢿⣿⣧⠀⠀⠀⠀⠀⢀⣶⠋⠀⠀⠀⠀⠀⠀⠀⠀⠀⠙⢦⡀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣯⣸⠿⢋⢧⡀⠀⠀⣰⡟⣡⣶⣶⣄⠀⠀⠀⠀⠀⠀⠀⠀⠀⠹⡄⠀⠀⠀⠀⠀⠀⣀⡀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠉⠙⠛⢶⣽⣦⣴⠏⣸⠛⡉⠙⠻⣿⣤⡀⠀⠀⠀⠀⠀⠀⣀⣽⡀⠀⠀⠀⢠⣾⣿⣷⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠹⣿⣏⣰⣿⢀⣚⣛⣻⣶⣿⣷⣄⠀⣀⣤⣤⣾⣿⠿⢿⣀⣠⠴⣿⣿⣿⣿⠂⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢠⡿⠀⠉⠻⢿⣼⣿⣇⣹⣿⠟⠋⠉⢻⣿⣿⣿⡿⣄⠀⢈⡴⠋⠉⠉⠉⠁⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣾⠀⢀⠀⠀⠀⠀⢉⣩⠙⠆⠀⠀⠀⠀⠙⠿⢽⣓⡛⠑⢻⡀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢠⡟⠀⢸⣾⣶⣶⣶⣿⣯⣴⣷⣄⠀⠀⠀⠀⠀⢰⡄⠀⠀⠀⢻⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣀⣼⢤⠶⢾⡿⣿⣄⠀⠈⠉⠙⠻⠿⢿⣶⠶⠶⠛⠛⠿⣦⣄⠀⢘⡇⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢀⣤⣄⣀⢀⣀⣴⣿⡇⢸⠀⢸⡇⠸⣯⠛⠶⢤⣄⣀⠀⠀⠀⠀⠀⠀⠀⠀⢈⢿⡇⠸⣄⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠐⠋⠉⠻⣿⣿⣿⣿⣿⣧⠸⣄⢀⣿⠛⠛⢷⡝⠲⢤⡈⠉⠑⠒⠒⠒⠒⠒⠛⠉⠘⠃⢰⣿⣦⡀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⢀⡴⠚⠁⠀⠀⠀⠀⠀⠛⣿⣿⣿⣿⣿⣧⠙⠚⣿⡆⠀⠈⢷⡐⠆⠀⠀⠀⠀⣀⠀⠀⠀⠀⠀⠀⠀⣼⣿⣿⣿⣶⣶⣶⣶⣦⡀
⠀⠀⠀⠀⠀⢠⡿⠁⠀⠀⠀⠀⠀⠀⠀⠀⠈⣿⣿⣿⣿⣿⣷⣴⣿⠇⠀⠀⢸⣇⣀⣀⡴⠂⠉⠀⠠⣄⠈⡆⠀⢀⣴⣿⣿⣿⣿⣿⠛⠁⠀⠈⠁
⠀⠀⠀⠀⠀⡾⠁⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠙⣿⣿⣿⣿⣿⣿⠋⠀⠀⠀⠋⠉⠁⠀⠀⠀⠀⠀⣀⣬⠿⠁⢠⣾⣿⣿⣿⣿⡟⠁⠀⠀⠀⠀⠀
⠀⠀⠀⠀⢸⠃⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣿⣿⣿⣿⣿⠇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠈⠋⠀⠀⣴⣿⣿⣿⣿⣿⡟⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⡞⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢸⣿⣿⣿⣿⣿⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠠⠀⣹⣿⣿⣏⣿⣿⡅⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⡇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢀⣤⣿⣿⣿⠟⠋⣥⠆⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠘⣿⣿⣿⢻⣿⣿⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⣰⠇⠀⠀⠀⠀⠀⣀⣀⠀⢀⡰⠞⠛⠉⠁⠀⠀⠀⢸⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢈⣿⣿⣤⣿⣿⣧⡤⠀⠀⠀⠀⠀⠀
⠀⠀⢠⡏⠀⠀⢀⡠⠀⠈⠁⠀⠈⠁⠀⠀⠀⠀⠀⠀⠐⠀⢹⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣼⣿⣿⣿⣿⣿⣟⣷⡆⠀⠀⠀⠀⠀
⠀⠀⣼⠁⠀⠠⠋⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢸⡄⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢹⣿⣿⣿⣿⣿⡿⠃⠀⡀⠀⠀⠀⠀
⠀⣰⠃⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡚⠖⠀⠸⡇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢀⢀⣴⣶⡟⠛⠛⠿⠿⠿⠿⠖⠒⠛⠓⠦⣄⡀
⣼⠋⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠙⣦⠐⠀⢿⡀⠀⠀⠀⠀⠀⠀⢀⣀⣠⣴⠿⠟⠋⠁⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠉
⣿⠁⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠈⢿⣄⣀⣤⣶⡾⠿⠟⠿⣏⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠹⣦⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡀⢠⣄⣠⡄⢢⣰⡜⠿⣿⠁⠉⠀⠀⠀⢸⣯⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⢿⣆⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠐⠀⠀⠈⠁⡾⣟⣿⡶⣌⡞⠀⠀⠀⠀⢸⣿⠂⠀⠂⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
