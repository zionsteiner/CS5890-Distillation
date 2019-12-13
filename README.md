### Steps to distill
1. Train teacher and student models with the Jupyter notebooks title 'cifar10_student/teacher_train_test.ipynb' to get 
model baseline performance. Save teacher model.
2. Collect teacher logits with 'get_logits_from_cifar10teacher.ipynb'.
3. Distill student with 'distill_cifar10.ipynb'. Modify parameter values and graph metrics here.
4. Distill student with a dilation factor (student = teacher * dilation) in 'distill_cifar_vary_size.ipynb'.

### Project progress
Using the CNN architecture found in 'cifar10_student/teacher_train_test.ipynb', distillation was not found to increase
the accuracy of a student model, as compared to a baseline. Instead, it seemed to hinder the training process instead of
aiding it. 

Future work might include experimenting with different datasets/architectures to see if changing these factors can achieve
positive results. After a successful version of the distillation process is implemented, it would be interesting to
work on augmenting it with other methods of model compression, such as weight pruning, quantization, and Hoffman encoding.

See Poster.pptx in the docs/ folder for more info on the results of this project.