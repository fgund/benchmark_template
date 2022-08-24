# benchmark_template
Template project for benchmarking using Conan

## Usage example:
1) mkdir build && cd build
2) conan install .. --build=missing
3) cmake .. -DCMAKE_TOOLCHAIN_FILE=conan_toolchain.cmake -DCMAKE_BUILD_TYPE=Release
4) cmake --build .

Write benchmark results to a file with the --benchmark_out=<filename> option (or set BENCHMARK_OUT). 
Specify the output format with --benchmark_out_format={json|console|csv} (or set BENCHMARK_OUT_FORMAT={json|console|csv}). 
Note that the 'csv' reporter is deprecated and the saved .csv file is not parsable by csv parsers.

Specifying --benchmark_out does not suppress the console output.