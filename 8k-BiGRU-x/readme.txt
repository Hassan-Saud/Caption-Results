Run epochs 250
Best results at epoch 250

Results at EPOCH 250:
BLUE-1 => 0.49
BLUE-2 => 0.26

Dataset => Flickr-8k

Train/Test split => 90% and 10%

Model:
Resnet50 -> Dense -> BatchNormalization -> Dense -> BatchNormalization -> BiGRU -> GRU -> Dense -> BatchNormalization -> Dense -> BatchNormalization -> Softmax

Results:
Captions are not so good. Maybe due to smaller dataset. Same model with bigger dataset gives good caption results.
Refer to the attahced folders for caption examples

Discussion:
	-> Model can be enhanced with more dense layers and increased no of neurons.
	-> Adam optimizer is used, different optimizers can be tried for their advantages.
	-> Xavier Normal initialization method is used for Weights Initialization, different methods like Xavier Uniform or any other can be used for their advantages
	-> 2 GRU layers are used, Although only one layer can also do good but the second layer further adds meaning to the captions by sequentially processing the combined (image_features + textual_features) input.
	-> ResNet50 is used for image features extraction, different CNNs can be used for their use cases and advantages like VGG, Inception, AlexNet etc.
	-> Trained on Flickr 8k dataset. This dataset contains 8,000 annotated images.
	-> This model can be tried on any real world image example.