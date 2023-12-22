Run for different epoochs 25,45, 55
Best results at epoch 45

Results at EPOCH 45:
BLUE-1 => 0.51
BLUE-2 => 0.27

Dataset => Flickr-30k

Train/Test split => 90% and 10%

Model:
Resnet50 -> Dense -> BatchNormalization -> Dense -> BatchNormalization -> BiGRU -> GRU -> Dense -> BatchNormalization -> Dense -> BatchNormalization -> Softmax

Captions:
Refer to the attahced folders for caption examples

Discussion:
	-> Model can be enhanced with more dense layers and increased no of neurons.
	-> Adam optimizer is used, different optimizers can be tried for their advantages.
	-> Xavier Normal initialization method is used for Weights Initialization, different methods like Xavier Uniform or any other can be used for their advantages
	-> 2 GRU layers are used, Although only one layer can also do good but the second layer further adds meaning to the captions by sequentially processing the combined (image_features + textual_features) input.
	-> ResNet50 is used for image features extraction, different CNNs can be used for their use cases and advantages like VGG, Inception, AlexNet etc.
	-> Trained on Flickr 30k dataset. This dataset contains 30,000 annotated images.
	-> This model can be tried on any real world image example.
	-> Model can be further trained if you have required computational resources.