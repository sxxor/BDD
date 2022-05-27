# Ejercicio BDD

# Autores: 
- Sara Ximena Ortiz Reyes
- Endi Romero
         
# Herramientas

- Framework .Net 3.5
- Visual Studio 2017
- Be.Corebvba.Aubergine.dll 1.0.0.0
- Gherkin


# Introducción
Simulador de cajero automático con escenarios parauna historia de usuario. retirar dinero con saldo y sin saldo y tarjeta invalida

# Instalación 

1. instalar SDK Net 3.5
2. visual studio 2017
3. Descargar o clonar el proyecto del respositorio
4. Ejecutar proyecto
5. el analisis final se genera al momento de compilarla solución


# Historia de usuario

private As_an Titular_Cuenta;
private I_want retirar_efectivo_de_un_cajero_automatico;
private So_that Poder_obtener_dinero_cuando_el_banco_este_cerrado;


- Escenario cuenta con fondos
- class La_Cuenta_tiene_fondos_suficientes_Para_Retiros : Scenario {
- Given el_saldo_de_la_cuenta_es_100;
- Given la_tarjeta_es_Valida;
- Given el_cajeroautomatico_contiene_suficiente_dinero;
- When el_titular_de_la_cuenta_solicita_20;
- Then el_cajero_automatico_debe_entregar_20;
- Then el_saldo_de_la_cuenta_debe_ser_80;
- Then entregar_tarjeta;
}


- Escenario cuenta sin fondos
- class Fondos_insuficientes_En_La_Cuenta : Scenario {
- Given el_saldo_de_la_cuenta_es_10;
- Given la_tarjeta_es_Valida;
- Given el_cajeroautomatico_contiene_suficiente_dinero;
- When el_titular_de_la_cuenta_solicita_20;
- Then el_cajero_automatico_no_debe_entregar_ningun_dinero;
- Then el_cajero_automatico_debe_decir_que_hay_fondos_insuficientes;
- Then el_saldo_de_la_cuenta_debe_ser_10;
- Then entregar_tarjeta;
}


# Conclusiones

1. Aprendimos a crear y configurar las BDD para un proyecto hecho en .net
2. Nos quedó mas claro el funcionamiento de las BDD y su utilización
