env = Environment(
    EM_HOME='/Users/chad/projects/emscripten',
    CC='$EM_HOME/emcc',
    CCFLAGS=['-Wall'],
    LINKFLAGS=['-s', 'FULL_ES2=1'],
    CXX='$EM_HOME/em++',
    OBJSUFFIX='.bc')

env.Program('lesson7.html', ['lesson7.cpp', 'tgaload.cpp'])
