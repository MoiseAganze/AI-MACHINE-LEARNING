# Plan accéléré : entraîner/fine-tuner des modèles IA open source
**Du 7 septembre au 30 novembre 2026 — 12 semaines, 5-10h/semaine (~90h total)**

## Philosophie du plan

Tu ne vas pas "entraîner des modèles from scratch" comme un labo avec 1000 GPU — personne ne fait ça hors des grosses boîtes. Tu vas apprendre à :
1. Comprendre assez de théorie pour savoir **quel outil/technique utiliser et pourquoi**
2. Maîtriser le **fine-tuning** (LoRA, QLoRA, fine-tuning complet sur petits modèles) — c'est 95% de ce qui se fait en pratique
3. Être autonome sur l'**infra cloud** (RunPod/Vast.ai) pour ne jamais être bloqué par le manque de GPU perso

Ordre : Fondamentaux → **Audio (approfondi)** → Image → Texte/LLM → Vidéo (survol). Chaque semaine a un objectif concret et un livrable, pas juste "lire de la théorie".

Budget cloud à prévoir : compte environ **50-150€ sur les 12 semaines** (RunPod facture à l'heure, un GPU type RTX 4090 coûte ~0,30-0,50€/h ; les gros runs A100 seront rares et ciblés).

---

## Semaine 1 — Bases PyTorch + boucle d'entraînement
**Objectif** : comprendre ce qui se passe réellement quand un modèle "s'entraîne".

- Tensors, autograd, `nn.Module`, `optimizer.step()`, `loss.backward()`
- Ressource clé : cours PyTorch officiel "60 min blitz" + premières vidéos de **Andrej Karpathy — "Neural Networks: Zero to Hero"** (excellent pour un débutant qui code déjà)
- Pratique : coder un petit classifieur (MNIST) from scratch, sans copier-coller passif — comprendre chaque ligne

**Livrable** : un notebook où tu entraînes et évalues un mini-réseau de zéro.

## Semaine 2 — Réseaux de neurones & attention (conceptuel)
- Backpropagation en profondeur (suite Karpathy : "micrograd", "makemore")
- Introduction à l'attention / self-attention (base des transformers, utile même pour l'audio moderne)
- Vidéo clé : Karpathy "Let's build GPT" (tu n'as pas besoin de tout maîtriser, juste l'intuition)

**Livrable** : schéma personnel (texte ou dessin) expliquant l'attention avec tes mots.

## Semaine 3 — Écosystème Hugging Face + premier fine-tuning "jouet"
- `transformers`, `datasets`, `accelerate`, `peft` (LoRA/QLoRA)
- Setup RunPod : créer un pod, choisir un GPU, se connecter en SSH/Jupyter, gérer le stockage persistant
- Premier fine-tuning simple sur un petit modèle texte (juste pour valider le pipeline cloud, pas pour la qualité)

**Livrable** : un pod RunPod fonctionnel + un fine-tuning terminé de bout en bout (même basique).

## Semaine 4 — Plongée Audio : concepts TTS & voice cloning
- Comprendre les familles de modèles TTS : autoregressifs (Tortoise, Bark) vs non-autoregressifs (VITS, StyleTTS2) vs flow-matching récents (F5-TTS, XTTS-v2)
- Comprendre le concept de "speaker embedding" pour le voice cloning
- Explorer et faire tourner (inférence seule) : **XTTS-v2 (Coqui)** ou **F5-TTS** en local via Colab ou RunPod

**Livrable** : générer un premier clip audio avec une voix clonée à partir d'un échantillon de 10-30s (juste inférence).

## Semaine 5-6 — Fine-tuning TTS en profondeur
- Préparer un dataset audio (nettoyage, transcription automatique avec Whisper, format attendu par le modèle)
- Fine-tuner XTTS-v2 ou F5-TTS sur une voix custom (LoRA si disponible, sinon fine-tuning léger)
- Debugger les problèmes classiques : qualité audio, accent, prosodie, overfitting sur un petit dataset

**Livrable (projet majeur #1)** : un modèle TTS fine-tuné capable de cloner une voix spécifique (la tienne, ou une voix libre de droits), avec un pipeline reproductible documenté.

## Semaine 7 — Musique / audio génératif
- Découvrir **MusicGen (Meta/AudioCraft)**, **AudioLDM**, **Stable Audio Open**
- Fine-tuning léger (LoRA) sur un style musical ou un genre spécifique
- Comprendre les différences avec le TTS (tokenisation audio, EnCodec, représentations latentes)

**Livrable** : génération de quelques secondes de musique dans un style choisi, avec ou sans fine-tuning léger.

## Semaine 8 — Bilan audio + consolidation infra
- Semaine "tampon" : rattraper le retard, optimiser tes scripts RunPod (templates réutilisables, docker si besoin)
- Documenter ton propre "playbook" personnel de fine-tuning audio (tu réutiliseras ce format pour les autres modalités)

**Livrable** : un repo GitHub perso avec tes scripts + un README "comment fine-tuner un modèle audio avec mon setup".

## Semaine 9 — Extension Image : diffusion & LoRA
- Concepts diffusion (denoising, U-Net, text encoder CLIP)
- Fine-tuning LoRA sur **Stable Diffusion / SDXL / Flux** via `diffusers` ou `kohya_ss`
- Beaucoup de concepts se transfèrent de l'audio (LoRA, datasets, RunPod déjà maîtrisé = gain de temps énorme ici)

**Livrable** : un LoRA image fine-tuné sur un style ou un sujet précis.

## Semaine 10 — Extension Texte : fine-tuning LLM
- QLoRA sur un petit LLM open source (Llama 3.x 8B, Mistral, Qwen) avec **Unsloth** (le plus simple/rapide pour débuter) ou **Axolotl**
- Comprendre le formatage des données d'instruction (chat templates)

**Livrable** : un petit LLM fine-tuné sur un dataset custom (ex : ton propre style d'écriture, ou un domaine spécifique).

## Semaine 11 — Vidéo : premier contact (survol volontaire)
- Panorama des modèles vidéo open source actuels (le domaine évolue vite — chercher l'état de l'art à ce moment-là plutôt que se fier à une liste figée)
- Inférence seule sur un modèle existant, éventuellement un LoRA très léger si le compute/temps le permet
- Objectif réaliste : comprendre le paysage et être capable de progresser seul plus tard, pas maîtriser

**Livrable** : une génération vidéo courte réussie via un modèle open source existant.

## Semaine 12 — Capstone & consolidation
- Choisir **un** projet parmi les 4 modalités pour aller plus loin en profondeur (recommandé : audio, ton point fort du plan)
- Nettoyer et documenter l'ensemble de ton repo/portfolio
- Bilan : lister ce que tu maîtrises, ce qu'il reste à approfondir, et un plan pour la suite (décembre et après)

**Livrable final** : un portfolio de 4 mini-projets (un par modalité) + un projet approfondi, tous reproductibles et documentés.

---

## Outils à installer/connaître dans l'ordre où tu les rencontres
- **PyTorch**, **Jupyter**
- **Hugging Face** : `transformers`, `datasets`, `accelerate`, `peft`
- **RunPod** ou **Vast.ai** (compte + carte bancaire, commence par de petits GPU pour apprendre l'interface)
- **Whisper** (transcription audio pour préparer tes datasets)
- **Coqui XTTS-v2** / **F5-TTS** (TTS)
- **AudioCraft (MusicGen)** (musique)
- **diffusers**, **kohya_ss** ou **ComfyUI** (image)
- **Unsloth** ou **Axolotl** (fine-tuning LLM)
- **Git/GitHub** pour versionner tes scripts et projets

## Conseils pratiques pour rester dans les 5-10h/semaine
- Privilégie toujours **faire tourner un exemple qui marche** avant de vouloir comprendre 100% de la théorie — tu apprends mieux en debuggant du concret
- Note systématiquement tes commandes RunPod/scripts dans un repo perso dès la semaine 3 — tu vas les réutiliser sans cesse
- Si une semaine déborde, coupe la théorie, pas la pratique
- Rejoins un ou deux serveurs Discord actifs sur le fine-tuning (Unsloth, Coqui/TTS, communautés Stable Diffusion) — énormément d'aide pratique s'y trouve gratuitement

## Ce qui ne sera PAS acquis au 30 novembre (soyons honnêtes)
- Une maîtrise mathématique profonde de chaque architecture
- La capacité à entraîner un modèle from scratch à grande échelle
- Une expertise vidéo (domaine encore jeune et coûteux en compute)

Ce qui SERA acquis : une **autonomie réelle** pour fine-tuner des modèles existants sur les 4 modalités, avec une vraie profondeur en audio, et la capacité à progresser seul ensuite sur n'importe quelle nouvelle modalité ou modèle qui sort.
