import math

def menu():
    print("Pour calculer l'aire d'un carré tapez 1." )
    print("Pour calculer l'aire d'un triangle tapez 2." )
    print("Pour calculer l'aire d'un cercle tapez 3." )
    print("Pour quitter tapez 0")
    choix=input("votre choix:")
   
    valid=False
    while  not valid:
        try:
            choix=int(choix)
            if choix in [0,1,2,3]:
                valid=True
            else:
                raise
    
        except:
            print("veuillez répondre par 0,1,2 ou 3")
            choix=input("votre choix :")

    
    
    if choix==1:
        aire_carre()
    elif choix==2:
        aire_triangle()
    elif choix==3:
        aire_cercle()
    elif choix==0:
        quit()

def quit():
    print("Adios le s")

def aire_carre():
    cote=input("Quelle est la longueur du coté de votre carré ?")
    cote=float(cote)
    aire=cote**2
    print(f"L'aire de votre carré vaut:{aire}")
    menu()

def aire_triangle():
    hauteur=input("Quelle est la hauteur de votre triangle ?")
    base=input("Quelle est la base du triangle")
    base=float(base)
    hauteur=float(hauteur)
    aire=base*hauteur/2
    print(f"L'aire de votre triangle vaut:{round(aire,4)}")
    menu()

def aire_cercle():
    rayon=input("Quelle est la longueur du rayon du cercle ?")
    rayon=float(rayon) 
    aire=math.pi*rayon**2
    print(f"L'aire de votre cercle vaut:{round(aire,4)}")
    menu()


if __name__=="__main__":
    menu() #execute la fonction menu
