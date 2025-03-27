## Introduction
Artificial intelligence (AI) is rapidly evolving in today’s age. M.A.V.I.S (My Average Very Intelligent System) is an AI-powered voice assistant designed to provide an engaging and interactive user experience. It is inspired by the fictional AI J.A.R.V.I.S from the Iron Man comics and movies. J.A.R.V.I.S is similar to traditional AI assistants like Siri and Google Assistant, but offers a more conversational and witty personality. Through the integration of speech-to-text, a fine-tuned large language model, waveform audio visualizations and text-to-speech synthesis, M.A.V.I.S offers dynamic and fun interactions through both auditory and visual feedback
In contrast to the majority of existing voice assistants that rely on rigid command-based systems, M.A.V.I.S is designed to take into account contextual awareness and user engagement. The model is offered as a mobile app. By leveraging open-source applications VOSK (speech recognition), RASA (natural language understanding), and Mozilla TTS (speech synthesis), the model balances performance, flexibility, and ethical AI principles. M.A.V.I.S is an AI system that not only understands user intent but also communicates in a human-like manner.
Our approach to creating M.A.V.I.S uses a sophisticated pipeline that transforms voice input into engaging interactions. It is a complete redesign of the typical AI assistant, from recording audio waveforms to generating smart responses and rendering speech output. We emphasize user interaction, accessibility, and ethics, and have created an AI assistant that has made technology interactions more responsive and engaging. 

## Related Works
When building M.A.V.I.S, we looked at a lot of other projects and research to understand what's already out there and where we could do something different. One of the biggest areas we focused on was the ethics of advanced AI assistants. A paper by Gabriel et al. (2024) brings up important questions about trust, misuse, and value alignment [(Gabriel et al., 2024)](https://arxiv.org/abs/2404.16244). That stuck with us, and it's why we’re putting a lot of emphasis on transparency, feedback loops, and diverse data from the start. We don’t want to just build something that works—we want it to be responsible and respectful of the people using it.

On the technical side, M.A.V.I.S uses a combination of VOSK for speech-to-text, RASA for natural language understanding, and Mozilla TTS for generating speech. This setup is pretty aligned with a few other projects, like My Assistant SRSTC [(IEEE Xplore)](https://ieeexplore.ieee.org/abstract/document/10593324) and another voice assistant built using GPT-3.5 and the Web Speech API [(IEEE Xplore)](https://ieeexplore.ieee.org/abstract/document/10545197). Those projects show how to stitch together the components of a speech pipeline, and they’ve been helpful in figuring out how to structure ours. The difference is that we’re going beyond just making the assistant functional—we’re adding personality, visual waveform feedback, and a more dynamic way of responding to users.

There’s also some cool research like LLaSM (Large Language and Speech Model) that tries to merge speech and text into a single training process [(arXiv)](https://arxiv.org/pdf/2308.15930). We're not doing exactly that, but it definitely influenced how we think about context in speech. While LLaSM is more focused on large-scale, instruction-following models, we’re focused on real-time interaction and creating an assistant that feels alive—more like J.A.R.V.I.S than a basic Q&A bot.

We also took inspiration from projects that focus on specific user groups. One study looked at how older adults interact with voice assistants, and it pointed out how rule-based models don’t always understand different speech patterns, especially as people age [(PubMed Central)](https://pmc.ncbi.nlm.nih.gov/articles/PMC11135128/). This made us think more about inclusivity and how we can make M.A.V.I.S flexible enough to work well for everyone—not just the tech-savvy.

Another interesting idea came from a paper about real-time emotion recognition in smart home assistants. They used things like MFCCs and CNNs to detect emotional tone in speech [(IEEE Xplore)](https://ieeexplore.ieee.org/abstract/document/9352018). We’re not fully there yet, but it got us thinking about how emotional awareness could be a future direction for M.A.V.I.S—making it not just smart, but empathetic and reactive in more human ways.

And finally, to help with some of the nuts and bolts of building this, we leaned on resources like *Natural Language Processing: An Introduction* [(ResearchGate)](https://www.researchgate.net/publication/51576224_Natural_language_processing_An_introduction). It’s more of a general guide, but it helped us troubleshoot and understand how to better structure our NLP models, especially when users go off-script or say something unexpected.

Overall, our approach to M.A.V.I.S blends what’s been done before with some fresh takes—like giving it a real personality, making it visually and auditorily engaging, and thinking through the ethical side from the beginning. It’s not just about building a tool, it’s about reimagining what interacting with AI could feel like.

## Ethical Sweep
General Questions: 
Should we even be doing this? Yes—if built responsibly, M.A.V.I.S can enhance user interaction and accessibility, but it requires careful oversight to ensure ethical use. 
What might be the accuracy of a simple non-ML alternative?  A non-ML approach would likely have lower accuracy and flexibility in understanding natural language compared to ML models. 
What processes will we use to handle appeals/mistakes? We plan to implement user feedback systems, clear error reporting channels, and regular reviews to correct issues and update the system. 
How diverse is our team? Our team includes members from various technical and creative backgrounds. 
How will we maintain transparency for the model?
We will document model decisions, communicate its limitations, and provide explanations for its generated responses when possible

Data Questions:
Is our data valid for its intended use? The data will require ongoing validation and updates to maintain its relevance and accuracy.
What bias could be in our data? The data may contain language, cultural, or demographic biases favoring certain perspectives over others which you must identify and address.
How could we minimize bias in our data and model? We can minimize bias by sourcing diverse and balanced datasets and applying bias detection techniques during training. This requires implementing comprehensive sampling strategies across different demographics, languages, and cultural contexts. Regular testing against known bias benchmarks and establishing feedback loops from diverse user groups will help identify and mitigate biases as they emerge. Additionally, maintaining transparent documentation about known limitations and potential bias areas will allow for ongoing improvement of the system.
How should we "audit" our code and data? You could implement automated testing, clear documentation, and human auditing of the system.
How can we ensure data security? If M.A.V.I.S was to be released at large scale, encryption for stored and transmitted data will be of utmost importance to ensure user privacy. We will also limit data retention and anonymize sensitive information.

Impact Questions:
Do we expect different error rates for different sub-groups in the data? Yes, variations in demographics can lead to different errors and subgroup testing could help.
What are likely misinterpretations of the results and what can be done to prevent those misinterpretations? Users may interpret the answers of the AI as definitive answers which can be mitigated with clear disclaimers.
How might we impinge individuals' privacy and/or anonymity? Handling the voice-to-text data is important and can be more secure with encryption.
What is the environmental impact of training and running M.A.V.I.S? All AI models require tons of computational power, which in turn has an energy cost. We will consider optimizing efficiency and minimizing energy use where possible.


## References

1. Gabriel, I., Manzini, A., Keeling, G., Hendricks, L. A., Rieser, V., Iqbal, H., ... & Manyika, J. (2024). *The Ethics of Advanced AI Assistants*. arXiv preprint arXiv:2404.16244. [https://arxiv.org/abs/2404.16244](https://arxiv.org/abs/2404.16244)

2. *LLASM: Large Language and Speech Model*. arXiv preprint arXiv:2308.15930. [https://arxiv.org/pdf/2308.15930](https://arxiv.org/pdf/2308.15930)

3. *Understanding Older People’s Voice Interactions with Smart Voice Assistants: A New Modified Rule-Based Natural Language Processing Model with Human Input*. [https://pmc.ncbi.nlm.nih.gov/articles/PMC11135128/](https://pmc.ncbi.nlm.nih.gov/articles/PMC11135128/)

4. *Natural Language Processing: An Introduction*. [https://www.researchgate.net/publication/51576224_Natural_language_processing_An_introduction](https://www.researchgate.net/publication/51576224_Natural_language_processing_An_introduction)

5. *Real-Time Speech Emotion Analysis for Smart Home Assistants*. [https://ieeexplore.ieee.org/abstract/document/9352018](https://ieeexplore.ieee.org/abstract/document/9352018)

6. *My Assistant SRSTC: Speech Recognition and Speech to Text Conversion*. [https://ieeexplore.ieee.org/abstract/document/10593324](https://ieeexplore.ieee.org/abstract/document/10593324)

7. *Artificial Intelligence-Based Chatbot with Voice Assistance*. [https://ieeexplore.ieee.org/abstract/document/10545197](https://ieeexplore.ieee.org/abstract/document/10545197)
