# GUIA para el uso de GIT en este Proyecto( usando GITFLOW ).

- mian-> rama principal -> PRD.
- develop -> rama principal nuevas funcinalidades.
- release -> rama para subir a PRD.
- hotfix/nombre-error-solucion -> rama de errores.
- feature/nuava-funcionalidad -> rama de nuevas funcinalidades.

## CASO #1: Error en produccion
1. Ir a rama main -> "git checkout main"
2. Hacer pull a la rama (main) -> "git pull".
3. Crear rama (hotfix/"nombre-del-cambio") -> "git branch hotfix/nombre-del-cambio".
4. Ir a rama (hotfix/nombre-del-cambio) -> "git checkout hotfix/nombre-del-cambio"
5. Hacer corrección y Probar.
6. Hacer commit -> "git add ." -> "git commit -m 'Iniciales del responsable ejemplo: WR: Texto descriptivo del commit.'"..
7. Hacer push a rama hotfix/nombre-del-cambio -> "git push origin hotfix/nombre-del-cambio".
8. Crear pull request de la rama (hotfix/nombre-del-cambio) a rama (main).
9. Aprobar y marge (si eres solo apruebas y merge, si es en equipo, el supervisor aprueba y hace el merge).
10. Crear pull request de la rama (hotfix/nombre-del-cambio) a rama (develop) y se habilita el borrado de la rama (hotfix/nombre-del-cambio) una ves se aprube y se haga el marge.
11. Aprobar y marge (si eres solo apruebas y merge, si es en equipo, el supervisor aprueba y hace el merge).
10. Ir a rama (main) y hacer pull -> "git checkout main" -> "git pull".
10. Guardar versión del proyecto -> Tag -> 'git tag -a v1.0.1 -m "Descripción de la versión"'.
11. Subir la versión del proyecto al remoto -> "git push origin v1.0.1".
12. Ir a la rama (develop) y hacer pull -> "git pull origin develop".

## CASO #2: Nuevas funcionalidades
1. Ir a la rama (develop) -> "git checkout develop".
2. Hacer pull a la rama (develop) -> "git pull origin develop".
3. Crear rama (feature/"nombre-nueva-funcionalidad") -> "git branch feature/nombre-nueva-funcionalidad".
4. Ir a rama (feature/nombre-nueva-funcionalidad) -> "git checkout feature/nombre-nueva-funcionalidad".
5. Crear la nueva funcionalidad y Probar.
6. Hacer commit -> "git add ." -> "git commit -m 'Iniciales del responsable ejemplo: WR: Texto descriptivo del commit.'"..
7. Hacer push a rama (feature/nombre-nueva-funcionalidad) -> "git push origin feature/nombre-nueva-funcionalidad".
8. Crear pull request de la rama (feature/nombre-nueva-funcionalidad) a rama (develop).
9. Aprobar y marge (si eres solo apruebas y merge, si es en equipo, el supervisor aprueba y hace el merge) y se habilita el borrado de la rama (feature/nombre-nueva-funcionalidad) una ves sea aprobada y se haga el marge.
10. Ir a rama (develop) y hacer pull -> "git checkout develop" -> "git pull origin develop".

## CASO #3: Generar release para pase a PRD
1. Ir a la rama (develop) -> "git checkout develop".
2. Hacer pull a la rama (develop) -> "git pull origin develop".
3. Crear rama (release) -> "git branch release".
4. Ir a rama (release) -> "git checkout release".
5. Pruebas -> todo Ok.
6. Hacer push a rama (release) -> "git push origin release".
7. Crear pull request de la rama (release) a rama (main).
8. Aprobar y marge (si eres solo apruebas y merge, si es en equipo, el supervisor aprueba y hace el merge) y se habilita el borrado de la rama (release) una ves sea aprobada y se haga el marge.
9. Ir a rama (main) y hacer pull -> "git checkout main" -> "git pull".
10. Guardar versión del proyecto -> Tag -> 'git tag -a v1.0.1 -m "Descripción de la versión"'.
11. Subir la versión del proyecto al remoto -> "git push origin v1.0.1".
12. Ir a la rama (develop) y hacer pull -> "git checkout develop" -> "git pull origin develop".

## CASO #3.1: Generar release para pase a PRD error en el release
1. Ir a la rama (develop) -> "git checkout develop".
2. Hacer pull a la rama (develop) -> "git pull origin develop".
3. Crear rama (release) -> "git branch release".
4. Ir a rama (release) -> "git checkout release".
5. Pruebas -> Si hay errores hacer cambios en la misma rama (release) -> "git add ." -> "git commit -m 'Iniciales del responsable ejemplo: WR: Texto descriptivo del commit.'"
6. Hacer push a rama (release) -> "git push origin release".
7. Crear pull request de la rama (release) a rama (main).
8. Aprobar y marge (si eres solo apruebas y merge, si es en equipo, el supervisor aprueba y hace el merge).
9. Crear pull request de la rama (release) a rama (develop).
10. Aprobar y marge (si eres solo apruebas y merge, si es en equipo, el supervisor aprueba y hace el merge) y se habilita el borrado de la rama (release) una ves sea aprobada y se haga el marge.
11. Ir a rama (main) y hacer pull -> "git checkout main" -> "git pull".
10. Guardar versión del proyecto -> Tag -> 'git tag -a v1.0.1 -m "Descripción de la versión"'.
11. Subir la versión del proyecto al remoto -> "git push origin v1.0.1".
12. Ir a la rama (develop) y hacer pull -> "git checkout develop" -> "git pull origin develop".