
########### next target ###############

SET(tesseract_neural_STAT_SRCS
   input_file_buffer.cpp
   neural_net.cpp
   neuron.cpp
   sigmoid_table.cpp
)

add_library(tesseract_neural_static STATIC ${tesseract_neural_STAT_SRCS})