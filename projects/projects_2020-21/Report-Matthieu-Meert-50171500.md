# Open Source Contribution Project
*Author :* Matthieu Meert

*Date :* November 2020

*NOMA :* 50171500

*Project :* [OpenShot Video Editor](https://github.com/OpenShot/openshot-qt)

## Finding a project to contribute to

So, we are in November and I haven't really looked for a project to contribute to yet. *Maybe I should have started earlier*. Let's go, easy peasy, I just need to find a project to contribute to, make something that is not too difficult or too long and it's in the pocket. I first think about contributing to software that I regularly use, which is more exciting, more rewarding and saves time as I already know the functionalities. My first thought is [Inkscape](https://inkscape.org/), a vectorial image editing software that I personnaly find amazing (go check it out, especially [this guy]( https://www.youtube.com/channel/UCEQXp_fcqwPcqrzNtWJ1w9w) if interested or if you hesitate to buy Adobe Illustrator)! So I go on their website (they don't seem active on github which is weird as the software is regularly updated), trying to find out how I can contribute. I am quickly redirected to other pages of the site and, a few clicks later (and a few new tabs opened), I finally discover that it is maintained on gitlab and that the base code is mainly written in C++ (which I'm not particularly comfortable with). Good news though, it is possible to write extensions using any language. Digging this possibility redirects me to some other pages. Finally, having about 8 tabs opened just to have a quick look on how to contribute, not any idea of an extension to make, the feeling that contributing to the main codebase will be too hard for me, it seems quite complicated and I am a bit discouraged about contributing to Inkscape. No problem, there are many fishes in the ocean, right?

Let's try to find something more suited for a first contribution. What could be best than the [github page](https://firstcontributions.github.io/#project-list) dedicated to firt contributions? So I am looking through the porposed projects, but every project either seems complicated or not really exciting for me to work on. *I should have started earlier*.

Back to square one. Which open-source softwares do I use, that could be good to make a first contribution? What about a game? A game is exciting, a game is fun, let's try to find a game. I remeber the old days, playing with my brother all the night on his computer, and this game "TuxKart", which is an open-source mariokart-like game using Tux (linux mascot) and other open-source mascots as main characters. I find out the original game is not maintained anymore but a fork named [SuperTuxKart](https://supertuxkart.net/Main_Page) is still active. So I install it, play a few hours, discover the new super cool "soccer" game mode, and then try to find out what I could do. It seems complicated as I am completely new to game development. Maybe I could create a new map or a new kart, but this would be really time-consuming. Looking at the issues on github is not encouraging as I have no idea what they are talking about, and it seems like it would take me days to do a 10 minutes job for someone who already knows the code. Maybe not worth it for a small contribution. Let's find another idea. *I should definitively have started earlier*.

Okay, keep calm, there must be something well suited for my first contribution. Why not combining this work and my master thesis? Indeed, I will implement a chatbot using an open-source framework, [Rasa](https://rasa.com/). This one is intersting, and surely well maintained, as I know that is has raised some money recently (13M in 2019 and 26M in 2020, as we can read in [source](https://voicebot.ai/2020/06/23/open-source-conversational-ai-startup-rasa-raises-26m-in-funding-round-led-by-andreessen-horowitz/)). I however decide not to contribute to this one for two main reasons: 
* It probably has very few easy to fix bugs, as many developers are hired to work on this
* I don't know much about language processing (yet), so it would take a lot of time for me just to understand the purpose of the library. *Not a single doubt about it, I should have started earlier*.

Despite the fact that I have not chosen this project to contribute to, I think it's an interesting example of how an open source project can evolve (in this case in an actual company), and even end up employing many full time developers, and still providing open source software. For more information about their business model, see this [page](https://rasa.com/how-we-make-money/) (which I advise you to read, truly interesting and perfect example of what we have seen in class).

Finally (yes, there is an end to this section), I think about this program I installed very recently to make a silly video montage for my "rallye chambre" activity. I opted for an open-source quick and easy to use program, [OpenShot Video Editor](https://www.openshot.org/). I remember being annoyed by the fact that SHIFT+scroll to scroll horizontally (which is particulatly useful in this kind of situation with a long horizontal timeline you have to scroll through all the time) was not implemented. This feature is widely used in other programs and is, in my opinion, a must have in that kind of program. This is perfect!

## Contact with the community

Next step is to follow the [instructions](https://github.com/OpenShot/openshot-qt/wiki/Become-a-Developer) to setup the project locally. This page is really clear and staightforward. As they ask for at the end of the instructions, I send an email to introduce myself. I am quickly added to the developer's chatroom in [Zulip](https://zulip.com/), an open-source alternative to Slack. The guy guides me with great care and support, and insists that I should create a PR as soon as I have questions or when I am stuck, even if it doesn't work yet. And so I start looking at the code to add this new feature.

## Getting into the code

It is not easy to get into the code of some huge progam that was written by others. My first idea is to look for a file that would give some explaination about the general structure of the code and the purppose of each part of it, which I don't find. Fortunately, some logs are appearing while doing things on the program, which quickly guides me to the part of the program I will have to change. CTRL+scroll was already implemented for zooming in/out, which is quite helpful to get the program to recognize SHIFT+scroll input! Based on that, I can easily implement the modification. Finally, at least for this enhancement, it is not needed for me to understand the whole program. Based on what is already implemented, it isn't very difficult to add this new feature.

## My contribution

Here is my [PR](https://github.com/OpenShot/openshot-qt/pull/3857). I took care that the correspondance of scrolling down/up resulting in moving right/left was consistent with what I have experienced in other programs. I also took care that the scroll speed is not proportional to time units but to the window, so that it doesn't scroll very fast when zommed in and very slow when zommed out. I am quite satisfied with the results. Even if it is simple, I think it can add a lot to the ease of use of the program. I look forward for the opinions/questions of the community on this!

## Feedback

After a few days, I receive a comment on my PR. Quite a surprise here, I am told that the feature is already implemented! It is still interesting to know that it doesn't work on some machines, and the next step will actually be to fix that bug more than add a new feature. Apparently, different backends have to be used depending on the OS. This also means that I will probably have to implement the feature differently, and in some other part of the code, specific for the backend used with my system.

So I start over on this new way of fixing the bug. It seems more complicated than before and, after a few hours of trying to fix it, I decide to take advice from the community. The maintainer who commented my PR is very active for the moment and seems to be the best person to suggest me some other ways I could try. His answers are really instructive and well explained, and our exchanges are always done with great care and courtesy. After trying some ways of solving the problem, he proposes a workaround. 

The bug is finally fixed and the PR is merged!

## Conclusion

The introduction part was intentionnaly long, to emphasise that there is a barrier of entry to contributing to open-source. I had difficulties making a step into it even though it was mendatory for this project. There are many reasons why someone would want to contribute and then finally be discouraged to do so. The introduction pointed out some of those reasons, and I hope this last part will give insights on how to mitigate them, both for maintainers of a project and for people that haven't contributed yet. 

I have learned many things with this project. I have pointed out some of them:

- When hesitating to contribute, it's a good idea to clone the repo and experiment with the code, it doesn't engage into anything.
- The community is generally very happy to have newcomers, and very friendly with them.
- The community is here to help you when you are stuck.
- Contributing doesn't mean spending days to understand the whole project (you don't have to understant everything to contribute).
- Contributing is exciting, rewarding, fun and social.
- Contributing seems far less compliacated when you have already done it once.
- Open source is everywhere around us.
- Open source is a whole world, and kind of a state of mind (it's amusing how the OpenShot's team like using open source whenever it's possible)

Finally, it is way funnier to contribute to a project you actually use than just contributing to anything to have the points for this course's project. I'm glad I have finally found such a project and very happy to have made my first contribution!

# Examen

J'ai décidé de parler de Rasa = framework qui permet d'automatiser des assistants textuels et vocaux (chatbot et assistant vocal).

## Pourquoi Rasa?

* je l'utilise pour mon mémoire
* le projet illustre bien plusieurs aspects du cours (notamment le business model)
* j'ai été impressionné par la vitesse d'évolution du projet et à quel point l'open source est central dans leur vision

## Création du projet 

* 2016, deux allemands
* chatbot = difficile -> frustrés des outils propriétaires disponibles 
    * pas si performants
    * pas si personnalisables
    * black box
    * risque de devenir payant/arrêt
* meetup group -> la plupart parlent de faire leur propre implémentation
* blog post sur comment le faire from scratch -> beaucoup d'intérêt mais personne ne le fait en pratique
* décident d'open sourcer leur propre implémentation
    * drop&replacement pour les API existantes
    * compatible, c'est facile de switcher
    * sous licence Apache 2.0

## Financements

 * 2019: obtiennent financement de $13M (Accel)
 * permet d'investir dans:
    * la communauté
    * le programme
    * la recherche
    * le département marketing
* sortie de Rasa X = outil gratuit mais propriétaire utilisé pour améliorer un assistant créé avec Rasa Open Source
* Rasa X est sous leur propre licence Rasa Community Edition License:
    * autorisé: utiliser à des fins commerciales ou privées, héberger
    * interdit: modifier, utiliser comme bas pour faire un outil de compétition, reverse engineering
* 2020:  second financement de $26M (Andreessen Horowitz)

## Business Model et Vision

Aujourd'hui, ils proposent 3 solutions:
* Rasa Open Soure: gratuit, open source -> permet de construire et entrainer un assistant performant
* Rasa X: gratuit, propriétaire -> permet d'avoir un feedback direct des utilisateurs, collecter et analyser les conversations des testeurs, utiliser un système de controle de versions intégré basé sur git
* Rasa Entreprise: payant, propriétaire -> contient tout ce qu'il y a dans Rasa Open Source et Rasa X, avec en plus des fonctionnalités qui répondent à la complexité organisationnelle d'une grande entreprise

Business Model = open core
* répartition juste des fonctionnalités entre les 3 produits
* "juste" = combiinaison de la valeur que les utilisateurs tirent du projet et les ressources qu'ils ont

Vision:
* objectif long terme = fournir la couche d'infrastructure standard pour l'IA conversationnelle
* faire une IA conversationnelle vraiment performante = très difficile, on y est pas encore du tout! 

    * chacun peut apporter sa pierre à l'édifice que ce soit en discutant/proposant des modifications/trouvant des erreurs/participant à la communauté, ou en prenant un contrat payant qui va permettre de faire avancer le travail et la recherche 

    * c'est un challenge global auquel on travaille tous ensemble!