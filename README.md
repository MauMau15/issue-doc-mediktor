# Problema con API mediktor para prediagnóstico

 En el siguiente documento se presenta como se ha respondido el mismo caso de prueba para el síntoma "Dolor de garganta" en ambas aplicaciones
 
 En la aplicación web de mediktor el prediagnóstico es mostrado sin problema alguno, pero en el caso de la aplicación móvil, llega a un punto en el que muestra el siguiente error:
 
````
{
  "error": {
    "code": "ME0",
    "description": "Ocurrió un error inesperado en el servidor. Por favor vuelva a intentarlo más tarde.",
    "retry": true
  }
}
````
 
El siguiente JSON corresponde a las respuestas que se enviaron a través de  la aplicación web de mediktor (el json es copia de la propiedad answers que se obtiene de la respuesta de la operación /answerStatement).
````
[
  {
    statementId: "b2427191-1078-470b-a869-542d2f6b9a78",
    description: "¿La evaluación es para usted?",
    descriptionShort: "¿La evaluación es para usted?",
    images: [],
    questionType: 1,
    hasDescriptionExtended: false,
    categoryIdList: [],
    response: "YES",
    answerSource: 0,
    responseOrder: 13,
    isActive: true,
    answerSourceValue: "USER",
  },
  {
    statementId: "015eee2f-bbfb-47a8-b1f7-9fa9a124a653",
    description: "Indique su edad",
    descriptionShort: "Edad en años",
    images: [],
    questionType: 7,
    multiAnswerMaxCount: 120,
    multiAnswerMinCount: 0,
    hasDescriptionExtended: false,
    categoryIdList: [],
    response: 25,
    answerSource: 0,
    responseOrder: 28,
    isActive: true,
    answerSourceValue: "USER",
  },
  {
    statementId: "6bd82c43-d080-4b3b-a64c-a1db09b4da4f",
    description: "¿Qué síntomas o signos siente?",
    descriptionShort: "¿Qué síntomas o signos siente?",
    images: [],
    questionType: 11,
    innerStatementList: [
      {
        statementId: "p10092v",
        description: "¿Le duele la garganta?",
        descriptionShort: "Dolor de garganta",
        images: [
          "https://int.mediktor.com/backoffice/downloads/File.Download?userId=0c6a1523-5b7f-389c-64ac-d7087cee8b0a&type=media&id=61de9e14-b533-4462-aef2-01d17afc56cd&d=1604075380327&b&l=1920",
        ],
        mediaFileList: [
          {
            mediaURL:
              "https://int.mediktor.com/backoffice/downloads/File.Download?userId=0c6a1523-5b7f-389c-64ac-d7087cee8b0a&type=media&id=61de9e14-b533-4462-aef2-01d17afc56cd&d=1604075380327&b&l=1920",
            copyright: "© Copyright TeckelMedical",
            description: "Dolor en garganta",
            type: 1,
          },
        ],
        questionType: 1,
        descriptionLarge:
          "<p>Dolor en la zona interna del cuello; puede aparecer&nbsp;espont&aacute;neamente o al tragar.&nbsp;</p>",
        descriptionExtended:
          "<p>Dolor en la zona interna del cuello; puede aparecer&nbsp;espont&aacute;neamente o al tragar.&nbsp;</p>",
        hasDescriptionExtended: true,
        categoryIdList: [],
        response: "YES",
        answerSource: 0,
        responseOrder: 104,
        responsibleStatementId: "6bd82c43-d080-4b3b-a64c-a1db09b4da4f",
        responsibleStatementIds: ["6bd82c43-d080-4b3b-a64c-a1db09b4da4f"],
        isActive: true,
        urgency: 5,
        answerSourceValue: "USER",
      },
    ],
    hasDescriptionExtended: false,
    response: "YES",
    answerSource: 0,
    responseOrder: 117,
    isActive: true,
    answerSourceValue: "USER",
  },
  {
    statementId: "7fa046c5-372f-46f3-923f-3d965d1ebbd0",
    description:
      "Indique la intensidad de su dolor utilizando la escala numérica, entre 1 dolor leve y 10 el peor dolor sentido nunca.",
    descriptionShort:
      "Indique la intensidad de su dolor utilizando la escala numérica, entre 1 dolor leve y 10 el peor dolor sentido nunca.",
    images: [],
    questionType: 4,
    innerStatementList: [
      {
        statementId: "4d027f02-6b42-4cf5-8512-d6085c82ec56",
        description:
          "¿El dolor es de intensidad moderada, interfiriendo es sus tareas cotidianas?",
        descriptionShort: "Dolor moderado",
        descriptionShortRelatedToResponsible: "Moderado 3-4",
        images: [
          "https://int.mediktor.com/backoffice/downloads/File.Download?userId=0c6a1523-5b7f-389c-64ac-d7087cee8b0a&type=media&id=9ca94c20-095e-448e-906d-88cef6bae170&d=1624433918938&b&l=1920",
        ],
        mediaFileList: [
          {
            mediaURL:
              "https://int.mediktor.com/backoffice/downloads/File.Download?userId=0c6a1523-5b7f-389c-64ac-d7087cee8b0a&type=media&id=9ca94c20-095e-448e-906d-88cef6bae170&d=1624433918938&b&l=1920",
            copyright: "© Copyright TeckelMedical",
            description: "Dolor moderado",
            type: 1,
          },
        ],
        questionType: 0,
        descriptionLarge:
          "<p>Si tuviera que puntuar la intensidad de su dolor del 0 al 10, tendr&iacute;a una intensidad entre 3&nbsp;y 4. (Entendiendo 0 como ausencia de dolor y 10 como el dolor m&aacute;s intenso posible).</p>",
        descriptionExtended:
          "<p>Si tuviera que puntuar la intensidad de su dolor del 0 al 10, tendr&iacute;a una intensidad entre 3&nbsp;y 4. (Entendiendo 0 como ausencia de dolor y 10 como el dolor m&aacute;s intenso posible).</p>",
        hasDescriptionExtended: true,
        categoryIdList: [],
        response: "YES",
        answerSource: 0,
        responseOrder: 121,
        responsibleStatementId: "7fa046c5-372f-46f3-923f-3d965d1ebbd0",
        responsibleStatementIds: ["7fa046c5-372f-46f3-923f-3d965d1ebbd0"],
        isActive: true,
        urgency: 4,
        answerSourceValue: "USER",
      },
    ],
    hasDescriptionExtended: false,
    categoryIdList: [],
    response: "YES",
    answerSource: 0,
    responseOrder: 120,
    isActive: true,
    answerSourceValue: "USER",
  },
  {
    statementId: "125",
    description: "¿Tiene dolor al tragar, por ejemplo al deglutir alimentos?",
    descriptionShort: "Dolor al tragar",
    images: [
      "https://int.mediktor.com/backoffice/downloads/File.Download?userId=0c6a1523-5b7f-389c-64ac-d7087cee8b0a&type=media&id=88c91039-4124-4c83-9fe0-f430ccd6f605&d=1605523901516&b&l=1920",
    ],
    mediaFileList: [
      {
        mediaURL:
          "https://int.mediktor.com/backoffice/downloads/File.Download?userId=0c6a1523-5b7f-389c-64ac-d7087cee8b0a&type=media&id=88c91039-4124-4c83-9fe0-f430ccd6f605&d=1605523901516&b&l=1920",
        copyright: "© Copyright TeckelMedical",
        description: "Dolor al tragar",
        type: 1,
      },
    ],
    questionType: 0,
    descriptionLarge:
      "<p>Cuando traga&nbsp;alimentos, bebidas o incluso saliva, siente dolor.&nbsp;</p><p>&nbsp;</p>",
    descriptionExtended:
      "<p>Cuando traga&nbsp;alimentos, bebidas o incluso saliva, siente dolor.&nbsp;</p><p>&nbsp;</p>",
    hasDescriptionExtended: true,
    categoryIdList: [],
    response: "YES",
    answerSource: 0,
    responseOrder: 127,
    isActive: true,
    urgency: 4,
    answerSourceValue: "USER",
  },
  {
    statementId: "cfa56221-eb05-4d4d-986a-381602f4b9a2",
    description: "Indique desde cuándo presenta los síntomas:",
    descriptionShort: "Indique desde cuándo presenta los síntomas:",
    images: [],
    questionType: 5,
    innerStatementList: [
      {
        statementId: "e0fba87a-8df4-47aa-a4fa-91ee43f66b27",
        description:
          "¿Los síntomas se han iniciado de manera muy rápida en minutos u horas?",
        descriptionShort: "Síntomas de inicio rápido - minutos / horas",
        descriptionShortRelatedToResponsible: "Horas",
        images: [],
        questionType: 0,
        hasDescriptionExtended: false,
        categoryIdList: [],
        response: "YES",
        answerSource: 0,
        responseOrder: 130,
        responsibleStatementId: "cfa56221-eb05-4d4d-986a-381602f4b9a2",
        responsibleStatementIds: ["cfa56221-eb05-4d4d-986a-381602f4b9a2"],
        isActive: true,
        urgency: 4,
        answerSourceValue: "USER",
      },
    ],
    hasDescriptionExtended: false,
    categoryIdList: [],
    response: "YES",
    answerSource: 0,
    responseOrder: 129,
    isActive: true,
    answerSourceValue: "USER",
  },
  {
    statementId: "086d9ba8-f0df-47ba-b676-f4462f065d1c",
    description: "Indique cuántas horas:",
    descriptionShort: "Horas de inicio de los síntomas",
    images: [],
    questionType: 7,
    hasDescriptionExtended: false,
    categoryIdList: [],
    response: 5,
    answerSource: 0,
    responseOrder: 139,
    isActive: true,
    answerSourceValue: "USER",
  },
  {
    statementId: "6e900f55-b54d-4930-9a8d-14dc530dd541",
    description:
      "¿Desde el inicio de los síntomas, cómo diría que evoluciona su estado?",
    descriptionShort:
      "¿Desde el inicio de los síntomas, cómo diría que evoluciona su estado?",
    images: [],
    questionType: 5,
    innerStatementList: [
      {
        statementId: "b3e051d0-3ceb-4b78-824f-88ea01edc2de",
        description:
          "¿La evolución es estable, los síntomas ni mejoran ni empeoran?",
        descriptionShort: "Estable, los síntomas ni mejoran ni empeoran",
        descriptionShortRelatedToResponsible:
          "Estable, los síntomas ni mejoran ni empeoran",
        images: [],
        questionType: 0,
        hasDescriptionExtended: false,
        categoryIdList: [],
        response: "YES",
        answerSource: 0,
        responseOrder: 174,
        responsibleStatementId: "6e900f55-b54d-4930-9a8d-14dc530dd541",
        responsibleStatementIds: ["6e900f55-b54d-4930-9a8d-14dc530dd541"],
        isActive: true,
        answerSourceValue: "USER",
      },
    ],
    hasDescriptionExtended: false,
    response: "YES",
    answerSource: 0,
    responseOrder: 173,
    isActive: true,
    answerSourceValue: "USER",
  },
  {
    statementId: "91",
    description: "¿Ha tenido fiebre o sensación de fiebre?",
    descriptionShort: "Sensación de fiebre",
    images: [
      "https://int.mediktor.com/backoffice/downloads/File.Download?userId=0c6a1523-5b7f-389c-64ac-d7087cee8b0a&type=media&id=5f620ae9-80e5-4a46-bb29-189aa45b029d&d=1604063802270&b&l=1920",
    ],
    mediaFileList: [
      {
        mediaURL:
          "https://int.mediktor.com/backoffice/downloads/File.Download?userId=0c6a1523-5b7f-389c-64ac-d7087cee8b0a&type=media&id=5f620ae9-80e5-4a46-bb29-189aa45b029d&d=1604063802270&b&l=1920",
        copyright: "© Copyright TeckelMedical",
        description: "Sensación de fiebre",
        type: 1,
      },
    ],
    questionType: 0,
    descriptionLarge:
      "<p>Es un aumento de la temperatura corporal.</p><p>Cuando aumenta unas d&eacute;cimas por encima de 37&ordm;C se denomina febr&iacute;cula&nbsp;y cuando supera los 38&ordm;C ya se considera fiebre.</p><p>Habitualmente&nbsp;la piel est&aacute;&nbsp;caliente al tacto y puede acompa&ntilde;arse de otros s&iacute;ntomas como debilidad, dolor muscular, dolor articular, dolor de cabeza, etc.</p>",
    descriptionExtended:
      "<p>Es un aumento de la temperatura corporal.</p><p>Cuando aumenta unas d&eacute;cimas por encima de 37&ordm;C se denomina febr&iacute;cula&nbsp;y cuando supera los 38&ordm;C ya se considera fiebre.</p><p>Habitualmente&nbsp;la piel est&aacute;&nbsp;caliente al tacto y puede acompa&ntilde;arse de otros s&iacute;ntomas como debilidad, dolor muscular, dolor articular, dolor de cabeza, etc.</p>",
    hasDescriptionExtended: true,
    categoryIdList: [],
    propertyValueList: [
      {
        propertyId: "cb6e1fc1-a673-4eab-8dec-4a483a473818",
        name: "Snomed",
        value: "386661006",
      },
    ],
    response: "NO",
    answerSource: 0,
    responseOrder: 177,
    isActive: true,
    answerSourceValue: "USER",
  },
  {
    statementId: "e0200761-0ca9-4a7e-a03e-5b17dc286421",
    description: "¿Tiene sensación de falta de aire?",
    descriptionShort: "Sensación de falta de aire",
    images: [
      "https://int.mediktor.com/backoffice/downloads/File.Download?userId=0c6a1523-5b7f-389c-64ac-d7087cee8b0a&type=media&id=a7ab9aa8-9d96-4d1d-82e3-7f52784439b3&d=1566979510209&b&l=1920",
    ],
    mediaFileList: [
      {
        mediaURL:
          "https://int.mediktor.com/backoffice/downloads/File.Download?userId=0c6a1523-5b7f-389c-64ac-d7087cee8b0a&type=media&id=a7ab9aa8-9d96-4d1d-82e3-7f52784439b3&d=1566979510209&b&l=1920",
        copyright: "© Copyright TeckelMedical",
        description: "Sensación de falta de aire - Disnea",
        type: 1,
      },
    ],
    questionType: 0,
    descriptionLarge:
      "<p>Tiene sensaci&oacute;n de ahogo, de que le falta ox&iacute;geno al respirar.&nbsp;</p>",
    descriptionExtended:
      "<p>Tiene sensaci&oacute;n de ahogo, de que le falta ox&iacute;geno al respirar.&nbsp;</p>",
    hasDescriptionExtended: true,
    categoryIdList: [],
    response: "NO",
    answerSource: 0,
    responseOrder: 179,
    isActive: true,
    answerSourceValue: "USER",
  },
  {
    statementId: "12b095b5-1849-4fad-b971-8a52a69454a9",
    description:
      "¿Tiene alguna alteración en la piel, por ejemplo enrojecimiento, una lesión, mancha o grano?",
    descriptionShort: "Alteración en la piel",
    images: [],
    questionType: 0,
    descriptionLarge:
      "<p>Le ha salido en alguna parte del cuerpo una mancha, herida, grano, rojez, aumento del color...que antes no ten&iacute;a.</p>",
    descriptionExtended:
      "<p>Le ha salido en alguna parte del cuerpo una mancha, herida, grano, rojez, aumento del color...que antes no ten&iacute;a.</p>",
    hasDescriptionExtended: true,
    categoryIdList: [],
    response: "NO",
    answerSource: 0,
    responseOrder: 180,
    isActive: true,
    answerSourceValue: "USER",
  },
  {
    statementId: "d287f4d9-9660-4ba1-bca8-3f2fc8d7499e",
    description:
      "¿Ha tomado alguna sustancia tóxica, como drogas, alcohol, medicamentos o alimentos potencialmente tóxicos?",
    descriptionShort: "Ingesta sustancia tóxica",
    images: [],
    questionType: 0,
    descriptionLarge:
      "<p>Incluye sustancias que en condiciones y/o en cantidades normales no resultar&iacute;an t&oacute;xicas, pero si lo son cuando su estado de conservaci&oacute;n no es el correcto o se ingieren en cantidades elevadas.</p><p>&nbsp;</p>",
    descriptionExtended:
      "<p>Incluye sustancias que en condiciones y/o en cantidades normales no resultar&iacute;an t&oacute;xicas, pero si lo son cuando su estado de conservaci&oacute;n no es el correcto o se ingieren en cantidades elevadas.</p><p>&nbsp;</p>",
    hasDescriptionExtended: true,
    categoryIdList: [],
    response: "NO",
    answerSource: 0,
    responseOrder: 226,
    isActive: true,
    answerSourceValue: "USER",
  },
  {
    statementId: "193k",
    description:
      "¿Tiene sensación de tener un objeto clavado en la garganta cuando hace el gesto de tragar?",
    descriptionShort: "Sensación de tener objeto clavado en la garganta",
    images: [
      "https://int.mediktor.com/backoffice/downloads/File.Download?userId=0c6a1523-5b7f-389c-64ac-d7087cee8b0a&type=media&id=6c9a3fd5-5cbc-478f-8065-444d2a6f1452&d=1572523503097&b&l=1920",
    ],
    mediaFileList: [
      {
        mediaURL:
          "https://int.mediktor.com/backoffice/downloads/File.Download?userId=0c6a1523-5b7f-389c-64ac-d7087cee8b0a&type=media&id=6c9a3fd5-5cbc-478f-8065-444d2a6f1452&d=1572523503097&b&l=1920",
        copyright: "© Copyright TeckelMedical",
        description: "Sensación de tener objeto clavado en garganta",
        type: 1,
      },
    ],
    questionType: 0,
    descriptionLarge:
      "<p>Por ejemplo, como si se le hubiera quedado una espina o hueso en la garganta y le molestara al tragar.</p>",
    descriptionExtended:
      "<p>Por ejemplo, como si se le hubiera quedado una espina o hueso en la garganta y le molestara al tragar.</p>",
    hasDescriptionExtended: true,
    categoryIdList: [],
    response: "UNK",
    answerSource: 0,
    responseOrder: 227,
    isActive: true,
    answerSourceValue: "USER",
  },
  {
    statementId: "d456u",
    description: "¿Tiene las amígdalas rojas y/o hinchadas?",
    descriptionShort: "Amígdalas rojas y/o hinchadas",
    images: [
      "https://int.mediktor.com/backoffice/downloads/File.Download?userId=0c6a1523-5b7f-389c-64ac-d7087cee8b0a&type=media&id=cc6677f0-4bd9-4efe-9c2b-714644112d0c&d=1531728492937&b&l=1920",
    ],
    mediaFileList: [
      {
        mediaURL:
          "https://int.mediktor.com/backoffice/downloads/File.Download?userId=0c6a1523-5b7f-389c-64ac-d7087cee8b0a&type=media&id=cc6677f0-4bd9-4efe-9c2b-714644112d0c&d=1531728492937&b&l=1920",
        copyright: "© Copyright TeckelMedical",
        description: "Amígdalas congestivas",
        type: 1,
      },
    ],
    questionType: 0,
    descriptionLarge:
      "<p>Si abre la boca, se ve la&nbsp;garganta roja e/o&nbsp;inflamada, incluso le duele al tragar.</p>",
    descriptionExtended:
      "<p>Si abre la boca, se ve la&nbsp;garganta roja e/o&nbsp;inflamada, incluso le duele al tragar.</p>",
    hasDescriptionExtended: true,
    categoryIdList: [],
    propertyValueList: [
      {
        propertyId: "cb6e1fc1-a673-4eab-8dec-4a483a473818",
        name: "Snomed",
        value: "281795003",
      },
    ],
    response: "UNK",
    answerSource: 0,
    responseOrder: 228,
    isActive: true,
    answerSourceValue: "USER",
  },
  {
    statementId: "p10092a",
    description: "¿Tiene irritación / inflamación de la faringe?",
    descriptionShort: "Irritación / inflamación de la faringe",
    images: [
      "https://int.mediktor.com/backoffice/downloads/File.Download?userId=0c6a1523-5b7f-389c-64ac-d7087cee8b0a&type=media&id=9026d2c1-fb12-4bb3-bd30-d6c7dcdd482a&d=1605264518227&b&l=1920",
      "https://int.mediktor.com/backoffice/downloads/File.Download?userId=0c6a1523-5b7f-389c-64ac-d7087cee8b0a&type=media&id=8b5a7c25-acbd-45d3-a417-cffcdb8476dc&d=1477779428028&b&l=1920",
    ],
    mediaFileList: [
      {
        mediaURL:
          "https://int.mediktor.com/backoffice/downloads/File.Download?userId=0c6a1523-5b7f-389c-64ac-d7087cee8b0a&type=media&id=9026d2c1-fb12-4bb3-bd30-d6c7dcdd482a&d=1605264518227&b&l=1920",
        copyright: "© Copyright TeckelMedical",
        description: "Irritación / inflamación de la faringe",
        type: 1,
      },
      {
        mediaURL:
          "https://int.mediktor.com/backoffice/downloads/File.Download?userId=0c6a1523-5b7f-389c-64ac-d7087cee8b0a&type=media&id=8b5a7c25-acbd-45d3-a417-cffcdb8476dc&d=1477779428028&b&l=1920",
        copyright: "© Copyright TeckelMedical",
        description: "Irritación / inflamación de la faringe",
        type: 1,
      },
    ],
    questionType: 0,
    descriptionLarge:
      "Por ejemplo, como cuando est&aacute; resfriado que le duele la garganta y le cuesta tragar.",
    descriptionExtended:
      "Por ejemplo, como cuando est&aacute; resfriado que le duele la garganta y le cuesta tragar.",
    hasDescriptionExtended: true,
    categoryIdList: [],
    response: "P_YES",
    answerSource: 0,
    responseOrder: 229,
    isActive: true,
    urgency: 5,
    answerSourceValue: "USER",
  },
  {
    statementId: "66cbea2a-0d78-460a-9189-b97ec2001c5c",
    description: "¿Ha presentado síntomas catarrales los 2-3 días previos?",
    descriptionShort: "Síntomas de flemas durante los 2-3 días previos",
    images: [],
    questionType: 0,
    descriptionLarge: "Mucosidad nasal, estornudos, tos y/o dolor de garganta.",
    descriptionExtended:
      "Mucosidad nasal, estornudos, tos y/o dolor de garganta.",
    hasDescriptionExtended: true,
    categoryIdList: [],
    response: "P_YES",
    answerSource: 0,
    responseOrder: 230,
    isActive: true,
    urgency: 5,
    answerSourceValue: "USER",
  },
  {
    statementId: "ba24a19c-e4b3-4896-ba68-907fe13a3071",
    description:
      "Indique si alguno de los siguientes desencadena o agrava la tos:",
    descriptionShort:
      "Indique si alguno de los siguientes desencadena o agrava la tos:",
    images: [],
    questionType: 5,
    innerStatementList: [
      {
        statementId: "10037",
        description: "¿Ha estado mucho tiempo en un ambiente frío y/o húmedo?",
        descriptionShort: "Exposición prolongada a frío y humedad",
        descriptionShortRelatedToResponsible: "Ambiente frío y húmedo",
        images: [],
        questionType: 0,
        descriptionLarge:
          "Por ejemplo, trabajando en c&aacute;maras frigor&iacute;ficas, subiendo un pico monta&ntilde;oso, viviendo en zonas donde llueve bastante, cerca del mar y/o en pa&iacute;ses o estaciones del a&ntilde;o donde las temperaturas son bajas.",
        descriptionExtended:
          "Por ejemplo, trabajando en c&aacute;maras frigor&iacute;ficas, subiendo un pico monta&ntilde;oso, viviendo en zonas donde llueve bastante, cerca del mar y/o en pa&iacute;ses o estaciones del a&ntilde;o donde las temperaturas son bajas.",
        hasDescriptionExtended: true,
        categoryIdList: [],
        response: "YES",
        answerSource: 0,
        responseOrder: 239,
        responsibleStatementId: "ba24a19c-e4b3-4896-ba68-907fe13a3071",
        responsibleStatementIds: ["ba24a19c-e4b3-4896-ba68-907fe13a3071"],
        isActive: true,
        urgency: 5,
        answerSourceValue: "USER",
      },
    ],
    hasDescriptionExtended: false,
    categoryIdList: [],
    response: "YES",
    answerSource: 0,
    responseOrder: 238,
    isActive: true,
    answerSourceValue: "USER",
  },
]
````

El siguiente JSON corresponde a las respuestas que se enviaron a través de  la aplicación móvil que estamos desarrollando (el json es copia de la propiedad answers que se obtiene de la respuesta de la operación /answerStatement).
````
[
  {
    statementId: "b2427191-1078-470b-a869-542d2f6b9a78",
    description: "¿La evaluación es para usted?",
    descriptionShort: "¿La evaluación es para usted?",
    images: [],
    questionType: 1,
    hasDescriptionExtended: false,
    categoryIdList: [],
    response: "YES",
    answerSource: 0,
    responseOrder: 5,
    isActive: true,
    answerSourceValue: "USER",
  },
  {
    statementId: "015eee2f-bbfb-47a8-b1f7-9fa9a124a653",
    description: "Indique su edad",
    descriptionShort: "Edad en años",
    images: [],
    questionType: 7,
    multiAnswerMaxCount: 120,
    multiAnswerMinCount: 0,
    hasDescriptionExtended: false,
    categoryIdList: [],
    response: 25,
    answerSource: 0,
    responseOrder: 20,
    isActive: true,
    answerSourceValue: "USER",
  },
  {
    statementId: "p10092v",
    description: "¿Le duele la garganta?",
    descriptionShort: "Dolor de garganta",
    images: [
      "https://int.mediktor.com/backoffice/downloads/File.Download?userId=0c6a1523-5b7f-389c-64ac-d7087cee8b0a&type=media&id=61de9e14-b533-4462-aef2-01d17afc56cd&d=1604075380327&b&l=1920",
    ],
    mediaFileList: [
      {
        mediaURL:
          "https://int.mediktor.com/backoffice/downloads/File.Download?userId=0c6a1523-5b7f-389c-64ac-d7087cee8b0a&type=media&id=61de9e14-b533-4462-aef2-01d17afc56cd&d=1604075380327&b&l=1920",
        copyright: "© Copyright TeckelMedical",
        description: "Dolor en garganta",
        type: 1,
      },
    ],
    questionType: 1,
    descriptionLarge:
      "<p>Dolor en la zona interna del cuello; puede aparecer&nbsp;espont&aacute;neamente o al tragar.&nbsp;</p>",
    descriptionExtended:
      "<p>Dolor en la zona interna del cuello; puede aparecer&nbsp;espont&aacute;neamente o al tragar.&nbsp;</p>",
    hasDescriptionExtended: true,
    categoryIdList: [],
    response: "YES",
    answerSource: 0,
    responseOrder: 109,
    isActive: true,
    urgency: 5,
    answerSourceValue: "USER",
  },
  {
    statementId: "6bd82c43-d080-4b3b-a64c-a1db09b4da4f",
    description: "¿Qué síntomas o signos siente?",
    descriptionShort: "¿Qué síntomas o signos siente?",
    images: [],
    questionType: 11,
    hasDescriptionExtended: false,
    response: "YES",
    answerSource: 0,
    responseOrder: 110,
    isActive: true,
    answerSourceValue: "USER",
  },
  {
    statementId: "78eb1876-4a5a-4c11-b73e-0aa899b0d993",
    description:
      "¿La intensidad de su dolor es tan leve que puede ser ignorado?",
    descriptionShort: "Dolor leve",
    images: [
      "https://int.mediktor.com/backoffice/downloads/File.Download?userId=0c6a1523-5b7f-389c-64ac-d7087cee8b0a&type=media&id=2e8b030d-83ef-49b3-89f4-6424e0d1dad0&d=1624433850102&b&l=1920",
    ],
    mediaFileList: [
      {
        mediaURL:
          "https://int.mediktor.com/backoffice/downloads/File.Download?userId=0c6a1523-5b7f-389c-64ac-d7087cee8b0a&type=media&id=2e8b030d-83ef-49b3-89f4-6424e0d1dad0&d=1624433850102&b&l=1920",
        copyright: "© Copyright TeckelMedical",
        description: "Dolor leve",
        type: 1,
      },
    ],
    questionType: 0,
    descriptionLarge:
      "Si tuviera que puntuar la intensidad de su dolor del 0 al 10, tendr&iacute;a una intensidad entre 1&nbsp;y 2 (entendiendo 0 como ausencia de dolor y 10 como el dolor m&aacute;s intenso posible).",
    descriptionExtended:
      "Si tuviera que puntuar la intensidad de su dolor del 0 al 10, tendr&iacute;a una intensidad entre 1&nbsp;y 2 (entendiendo 0 como ausencia de dolor y 10 como el dolor m&aacute;s intenso posible).",
    hasDescriptionExtended: true,
    categoryIdList: [],
    response: "unk",
    answerSource: 0,
    responseOrder: 124,
    isActive: true,
    urgency: 5,
    answerSourceValue: "USER",
  },
  {
    statementId: "4d027f02-6b42-4cf5-8512-d6085c82ec56",
    description:
      "¿El dolor es de intensidad moderada, interfiriendo es sus tareas cotidianas?",
    descriptionShort: "Dolor moderado",
    images: [
      "https://int.mediktor.com/backoffice/downloads/File.Download?userId=0c6a1523-5b7f-389c-64ac-d7087cee8b0a&type=media&id=9ca94c20-095e-448e-906d-88cef6bae170&d=1624433918938&b&l=1920",
    ],
    mediaFileList: [
      {
        mediaURL:
          "https://int.mediktor.com/backoffice/downloads/File.Download?userId=0c6a1523-5b7f-389c-64ac-d7087cee8b0a&type=media&id=9ca94c20-095e-448e-906d-88cef6bae170&d=1624433918938&b&l=1920",
        copyright: "© Copyright TeckelMedical",
        description: "Dolor moderado",
        type: 1,
      },
    ],
    questionType: 0,
    descriptionLarge:
      "<p>Si tuviera que puntuar la intensidad de su dolor del 0 al 10, tendr&iacute;a una intensidad entre 3&nbsp;y 4. (Entendiendo 0 como ausencia de dolor y 10 como el dolor m&aacute;s intenso posible).</p>",
    descriptionExtended:
      "<p>Si tuviera que puntuar la intensidad de su dolor del 0 al 10, tendr&iacute;a una intensidad entre 3&nbsp;y 4. (Entendiendo 0 como ausencia de dolor y 10 como el dolor m&aacute;s intenso posible).</p>",
    hasDescriptionExtended: true,
    categoryIdList: [],
    response: "YES",
    answerSource: 0,
    responseOrder: 125,
    isActive: true,
    urgency: 4,
    answerSourceValue: "USER",
  },
  {
    statementId: "774a1be5-7ea1-4f19-bba2-f2d2f8a03734",
    description: "¿Su dolor es tan intenso que afecta a su concentración?",
    descriptionShort: "Dolor intenso",
    images: [
      "https://int.mediktor.com/backoffice/downloads/File.Download?userId=0c6a1523-5b7f-389c-64ac-d7087cee8b0a&type=media&id=8fbb09b9-e542-4086-9505-1779a467e9a3&d=1624433599037&b&l=1920",
    ],
    mediaFileList: [
      {
        mediaURL:
          "https://int.mediktor.com/backoffice/downloads/File.Download?userId=0c6a1523-5b7f-389c-64ac-d7087cee8b0a&type=media&id=8fbb09b9-e542-4086-9505-1779a467e9a3&d=1624433599037&b&l=1920",
        copyright: "© Copyright TeckelMedical",
        description: "Dolor intenso",
        type: 1,
      },
    ],
    questionType: 0,
    descriptionLarge:
      "Si tuviera que puntuar la intensidad de su dolor del 0 al 10, tendr&iacute;a una intensidad entre 5 y 6. (Entendiendo 0 como ausencia de dolor y 10 como el dolor m&aacute;s intenso posible).",
    descriptionExtended:
      "Si tuviera que puntuar la intensidad de su dolor del 0 al 10, tendr&iacute;a una intensidad entre 5 y 6. (Entendiendo 0 como ausencia de dolor y 10 como el dolor m&aacute;s intenso posible).",
    hasDescriptionExtended: true,
    categoryIdList: [],
    response: "unk",
    answerSource: 0,
    responseOrder: 126,
    isActive: true,
    urgency: 5,
    answerSourceValue: "USER",
  },
  {
    statementId: "c6d64388-be57-4d47-bacc-b24f2b0e94f9",
    description: "¿El dolor es tan severo que resulta insoportable?",
    descriptionShort: "Dolor insoportable",
    images: [
      "https://int.mediktor.com/backoffice/downloads/File.Download?userId=0c6a1523-5b7f-389c-64ac-d7087cee8b0a&type=media&id=e263acb9-2748-4ec6-9e7e-3c6cfe70e9b5&d=1624433774251&b&l=1920",
    ],
    mediaFileList: [
      {
        mediaURL:
          "https://int.mediktor.com/backoffice/downloads/File.Download?userId=0c6a1523-5b7f-389c-64ac-d7087cee8b0a&type=media&id=e263acb9-2748-4ec6-9e7e-3c6cfe70e9b5&d=1624433774251&b&l=1920",
        copyright: "© Copyright TeckelMedical",
        description: "Dolor insoportable",
        type: 1,
      },
    ],
    questionType: 0,
    descriptionLarge:
      "Si tuviera que puntuar la intensidad de su dolor del 0 al 10, tendr&iacute;a una intensidad entre 7 y 8 (entendiendo 0 como ausencia de dolor y 10 como el dolor m&aacute;s intenso posible).",
    descriptionExtended:
      "Si tuviera que puntuar la intensidad de su dolor del 0 al 10, tendr&iacute;a una intensidad entre 7 y 8 (entendiendo 0 como ausencia de dolor y 10 como el dolor m&aacute;s intenso posible).",
    hasDescriptionExtended: true,
    categoryIdList: [],
    propertyValueList: [
      {
        propertyId: "cb6e1fc1-a673-4eab-8dec-4a483a473818",
        name: "Snomed",
        value: "76948002",
      },
    ],
    response: "unk",
    answerSource: 0,
    responseOrder: 127,
    isActive: true,
    urgency: 4,
    answerSourceValue: "USER",
  },
  {
    statementId: "cfea3515-52a2-454f-a3a0-5060dee7d77f",
    description: "¿Es el peor dolor imaginable?",
    descriptionShort: "Peor dolor imaginable",
    images: [
      "https://int.mediktor.com/backoffice/downloads/File.Download?userId=0c6a1523-5b7f-389c-64ac-d7087cee8b0a&type=media&id=44aef5f0-3303-43fb-835b-c36ba68edd8a&d=1624433977377&b&l=1920",
    ],
    mediaFileList: [
      {
        mediaURL:
          "https://int.mediktor.com/backoffice/downloads/File.Download?userId=0c6a1523-5b7f-389c-64ac-d7087cee8b0a&type=media&id=44aef5f0-3303-43fb-835b-c36ba68edd8a&d=1624433977377&b&l=1920",
        copyright: "© Copyright TeckelMedical",
        description: "Peor dolor imaginable",
        type: 1,
      },
    ],
    questionType: 0,
    descriptionLarge:
      "<p>Si tuviera que puntuar la intensidad de su dolor del 0 al 10, tendr&iacute;a una intensidad entre 9 y 10 (entendiendo 0 como ausencia de dolor y 10 como el dolor m&aacute;s intenso posible).</p>",
    descriptionExtended:
      "<p>Si tuviera que puntuar la intensidad de su dolor del 0 al 10, tendr&iacute;a una intensidad entre 9 y 10 (entendiendo 0 como ausencia de dolor y 10 como el dolor m&aacute;s intenso posible).</p>",
    hasDescriptionExtended: true,
    categoryIdList: [],
    propertyValueList: [
      {
        propertyId: "cb6e1fc1-a673-4eab-8dec-4a483a473818",
        name: "Snomed",
        value: "76948002",
      },
    ],
    response: "unk",
    answerSource: 0,
    responseOrder: 128,
    isActive: true,
    urgency: 3,
    answerSourceValue: "USER",
  },
  {
    statementId: "125",
    description: "¿Tiene dolor al tragar, por ejemplo al deglutir alimentos?",
    descriptionShort: "Dolor al tragar",
    images: [
      "https://int.mediktor.com/backoffice/downloads/File.Download?userId=0c6a1523-5b7f-389c-64ac-d7087cee8b0a&type=media&id=88c91039-4124-4c83-9fe0-f430ccd6f605&d=1605523901516&b&l=1920",
    ],
    mediaFileList: [
      {
        mediaURL:
          "https://int.mediktor.com/backoffice/downloads/File.Download?userId=0c6a1523-5b7f-389c-64ac-d7087cee8b0a&type=media&id=88c91039-4124-4c83-9fe0-f430ccd6f605&d=1605523901516&b&l=1920",
        copyright: "© Copyright TeckelMedical",
        description: "Dolor al tragar",
        type: 1,
      },
    ],
    questionType: 0,
    descriptionLarge:
      "<p>Cuando traga&nbsp;alimentos, bebidas o incluso saliva, siente dolor.&nbsp;</p><p>&nbsp;</p>",
    descriptionExtended:
      "<p>Cuando traga&nbsp;alimentos, bebidas o incluso saliva, siente dolor.&nbsp;</p><p>&nbsp;</p>",
    hasDescriptionExtended: true,
    categoryIdList: [],
    response: "YES",
    answerSource: 0,
    responseOrder: 132,
    isActive: true,
    urgency: 4,
    answerSourceValue: "USER",
  },
  {
    statementId: "e0fba87a-8df4-47aa-a4fa-91ee43f66b27",
    description:
      "¿Los síntomas se han iniciado de manera muy rápida en minutos u horas?",
    descriptionShort: "Síntomas de inicio rápido - minutos / horas",
    images: [],
    questionType: 0,
    hasDescriptionExtended: false,
    categoryIdList: [],
    response: "YES",
    answerSource: 0,
    responseOrder: 134,
    isActive: true,
    urgency: 4,
    answerSourceValue: "USER",
  },
  {
    statementId: "cfa56221-eb05-4d4d-986a-381602f4b9a2",
    description: "Indique desde cuándo presenta los síntomas:",
    descriptionShort: "Indique desde cuándo presenta los síntomas:",
    images: [],
    questionType: 5,
    hasDescriptionExtended: false,
    categoryIdList: [],
    response: "si",
    answerSource: 0,
    responseOrder: 135,
    isActive: true,
    answerSourceValue: "USER",
  },
  {
    statementId: "086d9ba8-f0df-47ba-b676-f4462f065d1c",
    description: "Indique cuántas horas:",
    descriptionShort: "Horas de inicio de los síntomas",
    images: [],
    questionType: 7,
    hasDescriptionExtended: false,
    categoryIdList: [],
    response: 5,
    answerSource: 0,
    responseOrder: 144,
    isActive: true,
    answerSourceValue: "USER",
  },
  {
    statementId: "b3e051d0-3ceb-4b78-824f-88ea01edc2de",
    description:
      "¿La evolución es estable, los síntomas ni mejoran ni empeoran?",
    descriptionShort: "Estable, los síntomas ni mejoran ni empeoran",
    images: [],
    questionType: 0,
    hasDescriptionExtended: false,
    categoryIdList: [],
    response: "YES",
    answerSource: 0,
    responseOrder: 178,
    isActive: true,
    answerSourceValue: "USER",
  },
  {
    statementId: "6e900f55-b54d-4930-9a8d-14dc530dd541",
    description:
      "¿Desde el inicio de los síntomas, cómo diría que evoluciona su estado?",
    descriptionShort:
      "¿Desde el inicio de los síntomas, cómo diría que evoluciona su estado?",
    images: [],
    questionType: 5,
    hasDescriptionExtended: false,
    response: "si",
    answerSource: 0,
    responseOrder: 179,
    isActive: true,
    answerSourceValue: "USER",
  },
  {
    statementId: "91",
    description: "¿Ha tenido fiebre o sensación de fiebre?",
    descriptionShort: "Sensación de fiebre",
    images: [
      "https://int.mediktor.com/backoffice/downloads/File.Download?userId=0c6a1523-5b7f-389c-64ac-d7087cee8b0a&type=media&id=5f620ae9-80e5-4a46-bb29-189aa45b029d&d=1604063802270&b&l=1920",
    ],
    mediaFileList: [
      {
        mediaURL:
          "https://int.mediktor.com/backoffice/downloads/File.Download?userId=0c6a1523-5b7f-389c-64ac-d7087cee8b0a&type=media&id=5f620ae9-80e5-4a46-bb29-189aa45b029d&d=1604063802270&b&l=1920",
        copyright: "© Copyright TeckelMedical",
        description: "Sensación de fiebre",
        type: 1,
      },
    ],
    questionType: 0,
    descriptionLarge:
      "<p>Es un aumento de la temperatura corporal.</p><p>Cuando aumenta unas d&eacute;cimas por encima de 37&ordm;C se denomina febr&iacute;cula&nbsp;y cuando supera los 38&ordm;C ya se considera fiebre.</p><p>Habitualmente&nbsp;la piel est&aacute;&nbsp;caliente al tacto y puede acompa&ntilde;arse de otros s&iacute;ntomas como debilidad, dolor muscular, dolor articular, dolor de cabeza, etc.</p>",
    descriptionExtended:
      "<p>Es un aumento de la temperatura corporal.</p><p>Cuando aumenta unas d&eacute;cimas por encima de 37&ordm;C se denomina febr&iacute;cula&nbsp;y cuando supera los 38&ordm;C ya se considera fiebre.</p><p>Habitualmente&nbsp;la piel est&aacute;&nbsp;caliente al tacto y puede acompa&ntilde;arse de otros s&iacute;ntomas como debilidad, dolor muscular, dolor articular, dolor de cabeza, etc.</p>",
    hasDescriptionExtended: true,
    categoryIdList: [],
    propertyValueList: [
      {
        propertyId: "cb6e1fc1-a673-4eab-8dec-4a483a473818",
        name: "Snomed",
        value: "386661006",
      },
    ],
    response: "NO",
    answerSource: 0,
    responseOrder: 182,
    isActive: true,
    answerSourceValue: "USER",
  },
  {
    statementId: "e0200761-0ca9-4a7e-a03e-5b17dc286421",
    description: "¿Tiene sensación de falta de aire?",
    descriptionShort: "Sensación de falta de aire",
    images: [
      "https://int.mediktor.com/backoffice/downloads/File.Download?userId=0c6a1523-5b7f-389c-64ac-d7087cee8b0a&type=media&id=a7ab9aa8-9d96-4d1d-82e3-7f52784439b3&d=1566979510209&b&l=1920",
    ],
    mediaFileList: [
      {
        mediaURL:
          "https://int.mediktor.com/backoffice/downloads/File.Download?userId=0c6a1523-5b7f-389c-64ac-d7087cee8b0a&type=media&id=a7ab9aa8-9d96-4d1d-82e3-7f52784439b3&d=1566979510209&b&l=1920",
        copyright: "© Copyright TeckelMedical",
        description: "Sensación de falta de aire - Disnea",
        type: 1,
      },
    ],
    questionType: 0,
    descriptionLarge:
      "<p>Tiene sensaci&oacute;n de ahogo, de que le falta ox&iacute;geno al respirar.&nbsp;</p>",
    descriptionExtended:
      "<p>Tiene sensaci&oacute;n de ahogo, de que le falta ox&iacute;geno al respirar.&nbsp;</p>",
    hasDescriptionExtended: true,
    categoryIdList: [],
    response: "NO",
    answerSource: 0,
    responseOrder: 184,
    isActive: true,
    answerSourceValue: "USER",
  },
  {
    statementId: "d287f4d9-9660-4ba1-bca8-3f2fc8d7499e",
    description:
      "¿Ha tomado alguna sustancia tóxica, como drogas, alcohol, medicamentos o alimentos potencialmente tóxicos?",
    descriptionShort: "Ingesta sustancia tóxica",
    images: [],
    questionType: 0,
    descriptionLarge:
      "<p>Incluye sustancias que en condiciones y/o en cantidades normales no resultar&iacute;an t&oacute;xicas, pero si lo son cuando su estado de conservaci&oacute;n no es el correcto o se ingieren en cantidades elevadas.</p><p>&nbsp;</p>",
    descriptionExtended:
      "<p>Incluye sustancias que en condiciones y/o en cantidades normales no resultar&iacute;an t&oacute;xicas, pero si lo son cuando su estado de conservaci&oacute;n no es el correcto o se ingieren en cantidades elevadas.</p><p>&nbsp;</p>",
    hasDescriptionExtended: true,
    categoryIdList: [],
    response: "NO",
    answerSource: 0,
    responseOrder: 185,
    isActive: true,
    answerSourceValue: "USER",
  },
  {
    statementId: "12b095b5-1849-4fad-b971-8a52a69454a9",
    description:
      "¿Tiene alguna alteración en la piel, por ejemplo enrojecimiento, una lesión, mancha o grano?",
    descriptionShort: "Alteración en la piel",
    images: [],
    questionType: 0,
    descriptionLarge:
      "<p>Le ha salido en alguna parte del cuerpo una mancha, herida, grano, rojez, aumento del color...que antes no ten&iacute;a.</p>",
    descriptionExtended:
      "<p>Le ha salido en alguna parte del cuerpo una mancha, herida, grano, rojez, aumento del color...que antes no ten&iacute;a.</p>",
    hasDescriptionExtended: true,
    categoryIdList: [],
    response: "NO",
    answerSource: 0,
    responseOrder: 186,
    isActive: true,
    answerSourceValue: "USER",
  },
  {
    statementId: "193k",
    description:
      "¿Tiene sensación de tener un objeto clavado en la garganta cuando hace el gesto de tragar?",
    descriptionShort: "Sensación de tener objeto clavado en la garganta",
    images: [
      "https://int.mediktor.com/backoffice/downloads/File.Download?userId=0c6a1523-5b7f-389c-64ac-d7087cee8b0a&type=media&id=6c9a3fd5-5cbc-478f-8065-444d2a6f1452&d=1572523503097&b&l=1920",
    ],
    mediaFileList: [
      {
        mediaURL:
          "https://int.mediktor.com/backoffice/downloads/File.Download?userId=0c6a1523-5b7f-389c-64ac-d7087cee8b0a&type=media&id=6c9a3fd5-5cbc-478f-8065-444d2a6f1452&d=1572523503097&b&l=1920",
        copyright: "© Copyright TeckelMedical",
        description: "Sensación de tener objeto clavado en garganta",
        type: 1,
      },
    ],
    questionType: 0,
    descriptionLarge:
      "<p>Por ejemplo, como si se le hubiera quedado una espina o hueso en la garganta y le molestara al tragar.</p>",
    descriptionExtended:
      "<p>Por ejemplo, como si se le hubiera quedado una espina o hueso en la garganta y le molestara al tragar.</p>",
    hasDescriptionExtended: true,
    categoryIdList: [],
    response: "UNK",
    answerSource: 0,
    responseOrder: 232,
    isActive: true,
    answerSourceValue: "USER",
  },
  {
    statementId: "d456u",
    description: "¿Tiene las amígdalas rojas y/o hinchadas?",
    descriptionShort: "Amígdalas rojas y/o hinchadas",
    images: [
      "https://int.mediktor.com/backoffice/downloads/File.Download?userId=0c6a1523-5b7f-389c-64ac-d7087cee8b0a&type=media&id=cc6677f0-4bd9-4efe-9c2b-714644112d0c&d=1531728492937&b&l=1920",
    ],
    mediaFileList: [
      {
        mediaURL:
          "https://int.mediktor.com/backoffice/downloads/File.Download?userId=0c6a1523-5b7f-389c-64ac-d7087cee8b0a&type=media&id=cc6677f0-4bd9-4efe-9c2b-714644112d0c&d=1531728492937&b&l=1920",
        copyright: "© Copyright TeckelMedical",
        description: "Amígdalas congestivas",
        type: 1,
      },
    ],
    questionType: 0,
    descriptionLarge:
      "<p>Si abre la boca, se ve la&nbsp;garganta roja e/o&nbsp;inflamada, incluso le duele al tragar.</p>",
    descriptionExtended:
      "<p>Si abre la boca, se ve la&nbsp;garganta roja e/o&nbsp;inflamada, incluso le duele al tragar.</p>",
    hasDescriptionExtended: true,
    categoryIdList: [],
    propertyValueList: [
      {
        propertyId: "cb6e1fc1-a673-4eab-8dec-4a483a473818",
        name: "Snomed",
        value: "281795003",
      },
    ],
    response: "UNK",
    answerSource: 0,
    responseOrder: 233,
    isActive: true,
    answerSourceValue: "USER",
  },
  {
    statementId: "66cbea2a-0d78-460a-9189-b97ec2001c5c",
    description: "¿Ha presentado síntomas catarrales los 2-3 días previos?",
    descriptionShort: "Síntomas de flemas durante los 2-3 días previos",
    images: [],
    questionType: 0,
    descriptionLarge: "Mucosidad nasal, estornudos, tos y/o dolor de garganta.",
    descriptionExtended:
      "Mucosidad nasal, estornudos, tos y/o dolor de garganta.",
    hasDescriptionExtended: true,
    categoryIdList: [],
    response: "P_YES",
    answerSource: 0,
    responseOrder: 234,
    isActive: true,
    urgency: 5,
    answerSourceValue: "USER",
  },
  {
    statementId: "10037",
    description: "¿Ha estado mucho tiempo en un ambiente frío y/o húmedo?",
    descriptionShort: "Exposición prolongada a frío y humedad",
    images: [],
    questionType: 0,
    descriptionLarge:
      "Por ejemplo, trabajando en c&aacute;maras frigor&iacute;ficas, subiendo un pico monta&ntilde;oso, viviendo en zonas donde llueve bastante, cerca del mar y/o en pa&iacute;ses o estaciones del a&ntilde;o donde las temperaturas son bajas.",
    descriptionExtended:
      "Por ejemplo, trabajando en c&aacute;maras frigor&iacute;ficas, subiendo un pico monta&ntilde;oso, viviendo en zonas donde llueve bastante, cerca del mar y/o en pa&iacute;ses o estaciones del a&ntilde;o donde las temperaturas son bajas.",
    hasDescriptionExtended: true,
    categoryIdList: [],
    response: "YES",
    answerSource: 0,
    responseOrder: 242,
    isActive: true,
    urgency: 5,
    answerSourceValue: "USER",
  },
  {
    statementId: "ba24a19c-e4b3-4896-ba68-907fe13a3071",
    description:
      "Indique si alguno de los siguientes desencadena o agrava la tos:",
    descriptionShort:
      "Indique si alguno de los siguientes desencadena o agrava la tos:",
    images: [],
    questionType: 5,
    hasDescriptionExtended: false,
    categoryIdList: [],
    response: "si",
    answerSource: 0,
    responseOrder: 243,
    isActive: true,
    answerSourceValue: "USER",
  },
]
````

A continuación, se presenta la manera en que se está enviando el cada JSON una vez que se recibe un tipo de respuesta

````
Body to send on new session
 {"apiVersion": "4.0.5", "appVersion": "1.5.2", "deviceId": "bea3e0a8-3c3b-4a56-92a6-2d5da53dd995", "deviceType": "WEB", "language": "es_MX", "locationRegion": "MX", "reason": "Dolor de garganta"}

Body to send, question type 1:
 {"apiVersion": "4.0.5", "appVersion": "1.5.2", "deviceId": "bea3e0a8-3c3b-4a56-92a6-2d5da53dd995", "deviceType": "WEB", "language": "es_MX", "preferredLanguage": "es", "responses": [{"response": "YES", "statementId": "b2427191-1078-470b-a869-542d2f6b9a78"}], "sessionId": "5575a96e-13ad-47d2-abaa-c767a1b1a996"}
 
Body to send, question type 7: 
 {"apiVersion": "4.0.5", "appVersion": "1.5.2", "deviceId": "bea3e0a8-3c3b-4a56-92a6-2d5da53dd995", "deviceType": "WEB", "language": "es_MX", "preferredLanguage": "es", "responses": [{"response": 25, "statementId": "015eee2f-bbfb-47a8-b1f7-9fa9a124a653"}], "sessionId": "5575a96e-13ad-47d2-abaa-c767a1b1a996"}
 
 
 Body to send, question type 11: 
 {"apiVersion": "4.0.5", "appVersion": "1.5.2", "deviceId": "bea3e0a8-3c3b-4a56-92a6-2d5da53dd995", "deviceType": "WEB", "language": "es_MX", "preferredLanguage": "es", "responses": [{"response": "YES", "statementId": "p10092v"}, {"response": "YES", "statementId": "6bd82c43-d080-4b3b-a64c-a1db09b4da4f"}], "sessionId": "5575a96e-13ad-47d2-abaa-c767a1b1a996"}
 
 Body to send, question type 4: 
 {"apiVersion": "4.0.5", "appVersion": "1.5.2", "deviceId": "bea3e0a8-3c3b-4a56-92a6-2d5da53dd995", "deviceType": "WEB", "language": "es_MX", "preferredLanguage": "es", "responses": [{"response": "unk", "statementId": "78eb1876-4a5a-4c11-b73e-0aa899b0d993"}, {"response": "YES", "statementId": "4d027f02-6b42-4cf5-8512-d6085c82ec56"}, {"response": "unk", "statementId": "774a1be5-7ea1-4f19-bba2-f2d2f8a03734"}, {"response": "unk", "statementId": "c6d64388-be57-4d47-bacc-b24f2b0e94f9"}, {"response": "unk", "statementId": "cfea3515-52a2-454f-a3a0-5060dee7d77f"}], "sessionId": "5575a96e-13ad-47d2-abaa-c767a1b1a996"}
 
Body to send, question type 0: 
 {"apiVersion": "4.0.5", "appVersion": "1.5.2", "deviceId": "bea3e0a8-3c3b-4a56-92a6-2d5da53dd995", "deviceType": "WEB", "language": "es_MX", "preferredLanguage": "es", "responses": [{"answerSource": 0, "response": "YES", "statementId": "125"}], "sessionId": "5575a96e-13ad-47d2-abaa-c767a1b1a996"}
 
 
 Body to send, question type 5: 
 {"apiVersion": "4.0.5", "appVersion": "1.5.2", "deviceId": "bea3e0a8-3c3b-4a56-92a6-2d5da53dd995", "deviceType": "WEB", "language": "es_MX", "preferredLanguage": "es", "responses": [{"response": "YES", "statementId": "e0fba87a-8df4-47aa-a4fa-91ee43f66b27"}, {"response": "si", "statementId": "cfa56221-eb05-4d4d-986a-381602f4b9a2"}], "sessionId": "5575a96e-13ad-47d2-abaa-c767a1b1a996"}
 
 Body to send, question type 7: 
 {"apiVersion": "4.0.5", "appVersion": "1.5.2", "deviceId": "bea3e0a8-3c3b-4a56-92a6-2d5da53dd995", "deviceType": "WEB", "language": "es_MX", "preferredLanguage": "es", "responses": [{"response": 5, "statementId": "086d9ba8-f0df-47ba-b676-f4462f065d1c"}], "sessionId": "5575a96e-13ad-47d2-abaa-c767a1b1a996"}
 
 
Body to send, question type 5: 
 {"apiVersion": "4.0.5", "appVersion": "1.5.2", "deviceId": "bea3e0a8-3c3b-4a56-92a6-2d5da53dd995", "deviceType": "WEB", "language": "es_MX", "preferredLanguage": "es", "responses": [{"response": "YES", "statementId": "b3e051d0-3ceb-4b78-824f-88ea01edc2de"}, {"response": "si", "statementId": "6e900f55-b54d-4930-9a8d-14dc530dd541"}], "sessionId": "5575a96e-13ad-47d2-abaa-c767a1b1a996"}
 
 
 Body to send, question type 0: 
 {"apiVersion": "4.0.5", "appVersion": "1.5.2", "deviceId": "bea3e0a8-3c3b-4a56-92a6-2d5da53dd995", "deviceType": "WEB", "language": "es_MX", "preferredLanguage": "es", "responses": [{"answerSource": 0, "response": "NO", "statementId": "91"}], "sessionId": "5575a96e-13ad-47d2-abaa-c767a1b1a996"}
 
 
 Body to send, question type 0: 
 {"apiVersion": "4.0.5", "appVersion": "1.5.2", "deviceId": "bea3e0a8-3c3b-4a56-92a6-2d5da53dd995", "deviceType": "WEB", "language": "es_MX", "preferredLanguage": "es", "responses": [{"answerSource": 0, "response": "NO", "statementId": "e0200761-0ca9-4a7e-a03e-5b17dc286421"}], "sessionId": "5575a96e-13ad-47d2-abaa-c767a1b1a996"}
 
 
 Body to send, question type 0: 
 {"apiVersion": "4.0.5", "appVersion": "1.5.2", "deviceId": "bea3e0a8-3c3b-4a56-92a6-2d5da53dd995", "deviceType": "WEB", "language": "es_MX", "preferredLanguage": "es", "responses": [{"answerSource": 0, "response": "NO", "statementId": "d287f4d9-9660-4ba1-bca8-3f2fc8d7499e"}], "sessionId": "5575a96e-13ad-47d2-abaa-c767a1b1a996"}
 
 
 Body to send, question type 0: 
 {"apiVersion": "4.0.5", "appVersion": "1.5.2", "deviceId": "bea3e0a8-3c3b-4a56-92a6-2d5da53dd995", "deviceType": "WEB", "language": "es_MX", "preferredLanguage": "es", "responses": [{"answerSource": 0, "response": "NO", "statementId": "12b095b5-1849-4fad-b971-8a52a69454a9"}], "sessionId": "5575a96e-13ad-47d2-abaa-c767a1b1a996"}
 
 
 Body to send, question type 0: 
 {"apiVersion": "4.0.5", "appVersion": "1.5.2", "deviceId": "bea3e0a8-3c3b-4a56-92a6-2d5da53dd995", "deviceType": "WEB", "language": "es_MX", "preferredLanguage": "es", "responses": [{"answerSource": 0, "response": "UNK", "statementId": "193k"}], "sessionId": "5575a96e-13ad-47d2-abaa-c767a1b1a996"}
 
 
 Body to send, question type 0: 
 * {"apiVersion": "4.0.5", "appVersion": "1.5.2", "deviceId": "bea3e0a8-3c3b-4a56-92a6-2d5da53dd995", "deviceType": "WEB", "language": "es_MX", "preferredLanguage": "es", "responses": [{"answerSource": 0, "response": "UNK", "statementId": "d456u"}], "sessionId": "5575a96e-13ad-47d2-abaa-c767a1b1a996"}
 
 
 Body to send, question type 0: 
 * {"apiVersion": "4.0.5", "appVersion": "1.5.2", "deviceId": "bea3e0a8-3c3b-4a56-92a6-2d5da53dd995", "deviceType": "WEB", "language": "es_MX", "preferredLanguage": "es", "responses": [{"answerSource": 0, "response": "P_YES", "statementId": "66cbea2a-0d78-460a-9189-b97ec2001c5c"}], "sessionId": "5575a96e-13ad-47d2-abaa-c767a1b1a996"}
 
 
 Body to send, question type 5: 
 {"apiVersion": "4.0.5", "appVersion": "1.5.2", "deviceId": "bea3e0a8-3c3b-4a56-92a6-2d5da53dd995", "deviceType": "WEB", "language": "es_MX", "preferredLanguage": "es", "responses": [{"response": "YES", "statementId": "10037"}, {"response": "si", "statementId": "ba24a19c-e4b3-4896-ba68-907fe13a3071"}], "sessionId": "5575a96e-13ad-47d2-abaa-c767a1b1a996"}
````



