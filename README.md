# Guitar_Audio_Descriptior_Detection

DESCRIPTION :

Ce project est un système d'analyse en temps réel du jeu instrumental pour un contrôle adaptatif d'effets sonore pour guitare. Notre inspiration principale est notre curiosité à utiliser les avancements en écoute et apprentissage machinique pour développer une façon d’interagir entre le jeu d'un interprète et ses effets audio.

CONTEXTE :

Ce projet de recherche-création a été réalisé à l'Université de Montréal dans le cadre du cours "MUS3329X-A-H26 - Projet en informatique musicale" enseigné par Dominic Thibault et David Piazza. Les auteurs du projet sont les étudiants :
- Raphaël Vinet-Quesnel 
- Simon St-Jules-Aillaud 
- Zao Dinel

OBJECTIF FINAL :

L'objectif final de ce projet est de contrôler une chaîne d'effets via un réseau neuronal. L'état actuel du projet se concentre sur l'identification et la classification des paramètres de jeu que l'on croit important à analyser.

CATÉGORISATION :

Nous avons classé les éléments en trois catégories - Couleur, Stabilité et Complexité - en nous inspirant de nos références, du jargon de guitariste, de notre perception de ce que ces éléments changent dans la façon de jouer et de bon sens afin que la classification soit intuitive pour des non-musiciens aussi. Notre organisation par dimension perceptive et musicale est une contribution propre à nous-même. 

Les spécificités du jeu sont divisées ainsi : 

COULEUR - éléments qui définissent le timbre de la guitare et la perception de celui-ci.
 - Tone d’attaque (softest à harshest/sharpest) / différent style de picking (doigts ou pick)
 - Richesse du timbre des notes / plus au moins d’harmoniques
 - Hauteur de la note en moyenne / registre moyen
 - Harmonicité~bruit / si le timbre du signal est bruité ou harmonique
 - Qualités des accord (Majeur / Mineur) - (l’analyse de cet élément n’est pas fonctionnelle en ce moment)

STABILITÉ - éléments qui font en sorte que le jeu de l’interprète peut sembler monotone ou varié.
- La valeur moyenne d'amplitude (10 dernière notes)
- Déviation / écart de l'amplitude de la dernière note contre le valeur d'amplitude moyenne
- Déviation / écart de la hauteur de la dernière note contre le registre moyen
- Déviation / écart de l’harmonicité de la dernière note contre l'harmonicité moyenne du timbre
- Régularité rythmique - (l’analyse de cet élément n’est pas fonctionnelle en ce moment)

COMPLEXITÉ - éléments qui semblent faire en sorte qu’un jeu peut être perçu comme simple ou complexe.
- Nombre de notes / attaques détectées par fenêtre variable (pourra éventuellement être associé au tempo de la session)
- Longueur des notes / Staccato, légato (pourra éventuellement être associé au tempo de la session)
- Longeur des espaces entre chaque note / pauses
- Temps entre chaque note / attaque détectée
- Quantité d’espace sur une fenêtre de temps variable (la somme des espaces / pauses entre chaque note à l’intérieur de la fenêtre est comparée à la longueur totale de la fenêtre) - (l’analyse de cet élément n’est pas fonctionnelle en ce moment)
- Nombre de note en même temps (lors d’un accord) / monophonie~polyphonie - (l’analyse de cet élément n’est pas fonctionnelle en ce moment)
- Détection des accord / nom exact de l’accord - (l’analyse de cet élément n’est pas fonctionnelle en ce moment)


LIBRAIRIE :



NOTE:

This hifheaibjkbegydalehdnalkcvailehdauelvlauglaeda iot and use it:

1) download FluCoMa from Max's package manager

2) download Pnp from Max's package manager

3) download [sigmund~] from [Max's package manager](https://github.com/v7b1/sigmund_64bit-version)

4) place this repo within the "MyExternals" folder inside MaxCpp

REFERENCE:

This project uses the c fft library KISS_FFT, MaxCpp (my update on Graham Wakefield's original), the Chromogram/Chord detector algorithms defined by Adam Stark, as well as the Max 7 SDK (by Cycling '74) -- all the credit for these open-source files should be give to their authors



THE PROJECT IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
