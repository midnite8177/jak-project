add_executable(decompiler
        main.cpp
        ObjectFile/ObjectFileDB.cpp
        Disasm/Instruction.cpp
        Disasm/InstructionDecode.cpp
        Disasm/OpcodeInfo.cpp
        Disasm/Register.cpp
        ObjectFile/LinkedObjectFileCreation.cpp
        ObjectFile/LinkedObjectFile.cpp
        Function/Function.cpp
        util/FileIO.cpp
        config.cpp
        util/DecompilerTypeSystem.cpp
        Function/BasicBlocks.cpp
        Disasm/InstructionMatching.cpp
        Function/CfgVtx.cpp Function/CfgVtx.h
        IR/BasicOpBuilder.cpp
        IR/CfgBuilder.cpp
        IR/IR.cpp)

target_link_libraries(decompiler
        goos
        minilzo
        common_util
        type_system
        fmt)