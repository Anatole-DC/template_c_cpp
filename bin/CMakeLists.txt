# To create executables:
#    add_executable(<name> source1 [source2 ...])
# To link existing libraries for compilation:
#    target_link_librairies(<name> source1 [source2 ...])

# To create bundles of sources:
#    set(<NAME> source1 [source2 ...])
# Then use ${NAME}

# To add all sources
file(GLOB_RECURSE SOURCES ../src/*.h ../src/*.cpp)
add_executable(executable main.cpp ${SOURCES})