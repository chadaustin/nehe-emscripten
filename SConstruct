
env = Environment()
env.Append(
    CCFLAGS=['-Wall', '-Werror'],
    FRAMEWORKS=['GLUT', 'OpenGL'])
env.Program('lesson7', ['lesson7.cpp', 'tgaload.cpp'])

SConscript('SConscript', variant_dir='em', duplicate=0)
