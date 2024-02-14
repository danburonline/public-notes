#lead/cognitivecomputing #core/machinelearning

![[proxy-tuning.png]]

Proxy-tuning is a technique designed to **fine-tune large language models (LLMs) at the decoding stage without changing the model’s internal weights.** This method involves adjusting the logits (the raw output values from the model’s final layer) of the target LLM by calculating the difference in logits between a smaller base model and **a fine-tuned version of that smaller model.** This difference is then added to the logits of the target model to improve its performance.

The process is particularly beneficial for scenarios where the large LLM is too resource-intensive to train or when the internal weights of the LLM are not accessible. Proxy-tuning allows for adapting LLMs to specific tasks or domains by leveraging smaller models, making it an efficient alternative to traditional fine-tuning methods.
