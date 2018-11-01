cmake_minimum_required(VERSION 3.12)

set(CMAKE_C_STANDARD 11)

set(C50_SOURCES global.c
                c50.c
                construct.c
                formtree.c
                info.c
                discr.c
                contin.c
                subset.c
                prune.c
                p-thresh.c
                trees.c
                siftrules.c
                ruletree.c
                rules.c
                getdata.c
                implicitatt.c
                mcost.c
                confmat.c
                sort.c
                update.c
                attwinnow.c
                classify.c
                formrules.c
                getnames.c
                modelfiles.c
                utility.c
                xval.c
                text.i)

set(REPORT_SOURCES report.c)

add_executable(C50 ${C50_SOURCES})
target_link_libraries(C50 m)

add_executable(xval ${C50_SOURCES})
target_link_libraries(xval m)

add_executable(report ${REPORT_SOURCES})
target_link_libraries(report m)
