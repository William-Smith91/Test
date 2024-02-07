import pandas as pd

# Utilisez une chaîne brute pour éviter les problèmes d'interprétation des caractères spéciaux
file_path = r"C:\Users\willi\Downloads\csv-template.csv"

print("Chemin du fichier :", file_path)

try:
    # Essayez de lire le fichier CSV avec pandas
    data = pd.read_csv(file_path)
    # Continuez avec le traitement ou l'analyse supplémentaire
except FileNotFoundError:
    # Gérez l'erreur si le fichier n'est pas trouvé
    print("Le fichier n'a pas été trouvé.")
except Exception as e:
    # Gérez d'autres erreurs possibles
    print("Une erreur s'est produite :", e)

