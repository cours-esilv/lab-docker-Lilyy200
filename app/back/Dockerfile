# Etape 1: Choisir l'image de base
FROM python:3.8-slim

# Etape 2: Définir le répertoire de travail
WORKDIR /app

# Etape 3: Copier le fichier requirements.txt dans l'image
# Adjust this path according to your project structure
COPY back/requirements.txt /app/

# Etape 4: Installer les dépendances
RUN pip install -r requirements.txt

# Etape 5: Copier le reste du code de l'application
# Ensure this copies everything you need into /app
COPY back /app

# Correctly set the FLASK_APP environment variable
ENV FLASK_APP=back/app.py

EXPOSE 5000

# Etape 6: Définir la commande par défaut
CMD ["python3", "-m", "flask", "run", "--host=0.0.0.0"]
