# Fall Week 8 — Linear Classification

## Presenter Notes

### Main ideas to emphasize

- A linear classifier separates the feature space using a straight decision boundary.
- The score $z = w^T x + b$ tells us which side of the boundary a point lies on.
- The sign of the score determines the predicted class.
- The weights `w` control the direction / orientation of the boundary.
- The bias `b` shifts the boundary.
- A perceptron-style classifier updates only when it makes a mistake.
- Training means repeatedly predicting, checking, and updating.
- Test accuracy matters because high training accuracy does not guarantee generalization.

### Common student confusion

- Students may confuse the score with the final class prediction.
  Emphasize that the score is a number first, then its sign becomes the class.

- Students may think `w` and `b` are arbitrary variables.
  Connect them directly to the geometry of the decision boundary.

- Students may not understand why an update changes the line.
  Show one manual update and connect the changed weights back to the plotted boundary.

- Students may assume more epochs always means better performance.
  Explain that training behavior depends on the data and model.

- Students may confuse training accuracy with test accuracy.
  Reinforce that the test set represents unseen examples.

### Suggested teaching flow

1. Start with the feature-space plot and ask students where they would draw a separating line.
2. Connect that line to the equation $w_1x_1 + w_2x_2 + b = 0$.
3. Compute one score manually.
4. Convert the score into a prediction.
5. Show one completed perceptron update.
6. Have students repeat the update on another example.
7. Build the prediction function.
8. Turn the update rule into a training loop.
9. Visualize how the boundary changes after training.
10. Compare training and test accuracy.
11. Finish by showing the sklearn `Perceptron` version.

### If students get stuck

- Reconnect the math to the picture.
- Ask which side of the boundary a point lies on.
- Work through one score and one update manually before returning to the loop.
- Keep helper plotting code completed so students can focus on the classifier logic.

### Timing

Core activity: about 15–20 minutes.

If time is limited, prioritize:
- score → prediction
- one manual update
- training loop
- learned boundary
- test accuracy

The sklearn comparison and final extension can be shortened if needed.

## Environment

Python 3 with NumPy, pandas, matplotlib, and scikit-learn.