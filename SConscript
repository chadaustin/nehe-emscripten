

env = Environment(
    EM_HOME='/Users/chad/projects/emscripten',
    CC='$EM_HOME/emcc',
    CCFLAGS=['-O1', '-Wall', '-fno-exceptions'],
    LINKFLAGS=[
        '-O1',
        '--llvm-lto', '1',
        '-g2',
        '--embed-file', 'CRATE.tga',
        '-s', 'FULL_ES2=1',
        '-s', 'ASM_JS=0',
        '-s', 'TOTAL_MEMORY=209715200',
        '-s', 'SAFE_DYNCALLS=1',
        '-s', 'ERROR_ON_UNDEFINED_SYMBOLS=1' ],
    CXX='$EM_HOME/em++',
    OBJSUFFIX='.bc')

env.Append(
    CPPDEFINES=[
        'REGAL_EMU_HINT=0',
        'REGAL_EMU_BIN=0',
        'REGAL_EMU_TEXSTO=0',
        'REGAL_EMU_DSA=0',
        'REGAL_EMU_PATH=0',
        #'REGAL_EMU_IFF=0',
        #'REGAL_EMU_SO=0',
        #'REGAL_EMU_VAO=0',
        #'REGAL_EMU_TEXC=0',
    
        'REGAL_NO_TLS',
        'REGAL_NO_PNG',
        'REGAL_NO_HTTP',
        'REGAL_NO_JSON',
        'REGAL_NO_TLS',
        'REGAL_NO_PNG',
        'REGAL_NO_HTTP',
        'REGAL_SYS_EMSCRIPTEN_STATIC' ],
    CPPPATH=[
        'regal/include',
        'regal/src/boost',
        'regal/src/lookup3',
        'regal/src/glu/include' ])

env.VariantDir('regal', '#/regal', duplicate=0)

REGAL_SOURCES = Split("""
    regal/src/glu/libutil/mipmap.c
    regal/src/glu/libutil/error.c
    regal/src/glu/libutil/glue.c
    regal/src/glu/libutil/project.c

    regal/src/jsonsl/jsonsl.c

    regal/src/regal/RegalHelper.cpp
    regal/src/regal/Regal.cpp
    regal/src/regal/RegalBreak.cpp
    regal/src/regal/RegalLog.cpp
    regal/src/regal/RegalCacheShader.cpp
    regal/src/regal/RegalCacheTexture.cpp
    regal/src/regal/RegalConfig.cpp
    regal/src/regal/RegalContext.cpp
    regal/src/regal/RegalContextInfo.cpp
    regal/src/regal/RegalDispatch.cpp
    regal/src/regal/RegalDispatchCache.cpp
    regal/src/regal/RegalDispatchCode.cpp
    regal/src/regal/RegalDispatchDebug.cpp
    regal/src/regal/RegalDispatchEmu.cpp
    regal/src/regal/RegalDispatchError.cpp
    regal/src/regal/RegalDispatchLog.cpp
    regal/src/regal/RegalUtil.cpp
    regal/src/regal/RegalDispatchStaticES2.cpp
    regal/src/regal/RegalDispatcher.cpp
    regal/src/regal/RegalDispatcherGL.cpp
    regal/src/regal/RegalEmu.cpp
    regal/src/regal/RegalEmuInfo.cpp
    regal/src/regal/RegalHelper.cpp
    regal/src/regal/RegalHttp.cpp
    regal/src/regal/RegalIff.cpp
    regal/src/regal/RegalInit.cpp
    regal/src/regal/RegalLog.cpp
    regal/src/regal/RegalQuads.cpp
    regal/src/regal/RegalSo.cpp


    regal/src/regal/RegalTexC.cpp
    regal/src/regal/RegalToken.cpp
    regal/src/regal/RegalUtil.cpp
    regal/src/regal/RegalXfer.cpp
    regal/src/regal/RegalFilt.cpp
""")

env.Program('lesson7.html', ['lesson7.cpp', 'tgaload.cpp'] + REGAL_SOURCES)
