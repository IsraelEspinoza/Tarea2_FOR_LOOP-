# Tarea2_FOR_LOOP-
#Subida de datas
Pequena_per <- read_excel("GitHub/Pequena_peru.xlsx")
Pequena_col <-read_excel("GitHub/Pequena_colombia.xlsx")
Pequena_chi <-read_excel("GitHub/Pequena_chile.xlsx")
Micro_per <-read_excel("GitHub/Micro_peru.xlsx")
Micro_col <-read_excel("GitHub/Micro_colombia.xlsx")
Micro_chi <-read_excel("GitHub/Micro_chile.xlsx")
Medianas_per <-read_excel("GitHub/Medianas_peru.xlsx")
Medianas_col <-read_excel("GitHub/Medianas_colombia.xlsx")
Medianas_chi <-read_excel("GitHub/Medianas_chile.xlsx")
Grandes_per <-read_excel("GitHub/Grandes_peru.xlsx")
Grandes_col <-read_excel("GitHub/Grandes_colombia.xlsx")
Grandes_chi <-read_excel("GitHub/Grandes_chile.xlsx")

#Crear variable tamaño
pequena_per <- mutate(Pequena_per, tamanio="pequeña")
pequena_col <- mutate(Pequena_col, tamanio="pequeña")
pequena_chi <- mutate(Pequena_chi, tamanio="pequeña")
micro_per <- mutate(Micro_per, tamanio="micro")
micro_col <- mutate(Micro_col, tamanio="micro")
micro_chi <- mutate(Micro_chi, tamanio="micro")
medianas_per <- mutate(Medianas_per, tamanio="mediana")
medianas_col <- mutate(Medianas_col, tamanio="mediana")
medianas_chi <- mutate(Medianas_chi, tamanio="mediana")
grandes_per <- mutate(Grandes_per, tamanio="grande")
grandes_col <- mutate(Grandes_col, tamanio="grande")
grandes_chi <- mutate(Grandes_chi, tamanio="grande")

#Unir datas en una sola base
names(pequena_per)
names(pequena_col)
names(pequena_chi)
names(micro_chi)
names(medianas_per)
names(medianas_chi)
names(grandes_per)
names(grandes_col)
names(grandes_chi)
pequena_per <-rename(pequena_per,porcentaje_mujeres=procentaje_mujeres)
micro_chi <- rename(micro_chi,porcentaje_mujeres=procentaje_muejeres)
medianas_per <- rename(medianas_per, porcentaje_mujeres=procentaje_muejeres)
medianas_chi <- rename(medianas_chi, porcentaje_mujeres=procentaje_mujeres)
grandes_per <- rename(grandes_per,porcentaje_mujeres=procentaje_muejeres)
grandes_col <- rename(grandes_col, porcentaje_mujeres=procentaje_mujeres)
grandes_chi <- rename(grandes_chi, porcentaje_mujeres=procentaje_mujeres)

base <- rbind(pequena_per,pequena_col,pequena_chi,micro_per,micro_col,
micro_chi,medianas_per,medianas_col,medianas_chi,grandes_per,grandes_col, grandes_chi)


str(base)











