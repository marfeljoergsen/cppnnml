This is slightly modified from: https://github.com/intel/cppnnml/wiki/A-Neural-Network-In-Under-4KB

cd ~/Downloads/cppnnml
mkdir build

cd ~/Downloads/cppnnml/examples/xor
g++ -O3 -o ../../build/xor xor.cpp xornet.cpp ../../cpp/lookupTables.cpp -DENABLE_OSTREAMS -DTINYMIND_USE_TANH_8_8 -I../../cpp -I../../apps/include

Running "./xor" generates the result "nn_fixed_xor.txt". 

Try to read it:
python ../unit_test/nn/nn_plot.py nn_fixed_xor.txt

In case of "ModuleNotFoundError: No module named 'PIL'", for Arch Linux: "yay -S python-image"

