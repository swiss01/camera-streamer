catch2_dep = declare_dependency(
    include_directories: '3rdparty/Catch2'
)

test_files = {
    'basic test'      : files('test.cpp'),
    'flags test'      : files('test_flags.cpp'),
    'aliases test'    : files('test_aliases.cpp'),
    'containers test' : files('test_containers.cpp'),
}

foreach test_name, test_src : test_files
    test_exe = executable(
        test_name.underscorify(),
        test_src,

        dependencies: [magic_enum_dep, catch2_dep]
    )

    test(test_name, test_exe)
endforeach
