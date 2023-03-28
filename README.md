# hse_hw3_chromhmm

[Ссылка на юпитер ноутбук](https://colab.research.google.com/drive/1HkCd_co11wWraCrXl8VCUSWFs5tL6wHh?usp=sharing)

## Гистоновые Метки

| Имя      | Файл                                                 |
|----------|------------------------------------------------------|
| H2AFZ    | wgEncodeBroadHistoneA549H2azDex100nmAlnRep1.bam      |
| H3k27ac  | wgEncodeBroadHistoneA549H3k27acDex100nmAlnRep1.bam   |
| H3k27me3 | wgEncodeBroadHistoneA549H3k27me3Dex100nmAlnRep1.bam  |
| H3k36me3 | wgEncodeBroadHistoneA549H3k36me3Dex100nmAlnRep1.bam  |
| H3k04me1 | wgEncodeBroadHistoneA549H3k04me1Dex100nmAlnRep1.bam  |
| H3k04me2 | wgEncodeBroadHistoneA549H3k04me2Dex100nmAlnRep1.bam  |
| H3k04me3 | wgEncodeBroadHistoneA549H3k04me3Dex100nmAlnRep1.bam  |
| H3k79me2 | wgEncodeBroadHistoneA549H3k79me2Dex100nmAlnRep1.bam  |
| H3k09ac  | wgEncodeBroadHistoneA549H3k09acEtoh02AlnRep1.bam     |
| H3k09me3 | wgEncodeBroadHistoneA549H3k09me3Etoh02AlnRep1.bam    |

## [cellmarkfiletable.txt](https://github.com/Kcchernikov/hse_hw3_chromhmm/blob/main/data/cellmarkfiletable.txt)

| Клеточная линия | Гистоновая метка | Файл с меткой | Файл с контролем |
|-----------------|------------------|---------------|------------------|
| A549	          | H2AFZ	           | H2AFZ.bam	   | Control.bam      |
| A549	          | H3k79me2	       | H3k79me2.bam	 | Control.bam      |
| A549	          | H3k04me2	       | H3k04me2.bam	 | Control.bam      |
| A549	          | H3k04me1	       | H3k04me1.bam	 | Control.bam      |
| A549	          | H3k36me3	       | H3k36me3.bam	 | Control.bam      |
| A549	          | H3k27me3	       | H3k27me3.bam	 | Control.bam      |
| A549	          | H3k27ac	         | H3k27ac.bam	 | Control.bam      |
| A549	          | H3k09ac	         | H3k09ac.bam	 | Control.bam      |
| A549	          | H3k09me3	       | H3k09me3.bam	 | Control.bam      |
| A549	          | H3k04me3	       | H3k04me3.bam	 | Control.bam      |

## ChromHMM

### Emission
<img width="348" alt="image" src="https://user-images.githubusercontent.com/80039707/228235482-53782bf5-470c-438f-a47a-633d652d34db.png">

### Transition Parameters
<img width="362" alt="image" src="https://user-images.githubusercontent.com/80039707/228235841-1fcc4a73-d97e-4916-b0b6-f7a48b14472b.png">

### Overlap
<img width="420" alt="image" src="https://user-images.githubusercontent.com/80039707/228236034-9507fb08-fe30-4c80-bba4-6cb0934272a3.png">

### RefSeqTSS
<img width="698" alt="image" src="https://user-images.githubusercontent.com/80039707/228236157-c9ea9808-c9c3-4b16-a0f3-6158405c2ae4.png">

### RefSeqTES
<img width="703" alt="image" src="https://user-images.githubusercontent.com/80039707/228236231-c941cc08-fb6b-4ccf-8408-f708c88c8079.png">

## Эпигенетические типы

### Тип 1
<img width="981" alt="image" src="https://user-images.githubusercontent.com/80039707/228281267-259d9f73-1056-4c6a-872e-b7dfe254da92.png">
Polycomb-repressed. Чаще всего находятся на ядерной ламине, попадает на репрессированный участок. Выражен на H3k27me3. Не попадает на ген (видно на overlap)

### Тип 2
<img width="965" alt="image" src="https://user-images.githubusercontent.com/80039707/228275319-f79b7f37-b318-450b-86e1-184211a2d66d.png">
Polycomb-repressed. Чаще всего находятся на ядерной ламине, попадает на репрессированный участок. Не попадает на ген (видно на overlap)

### Тип 3
<img width="958" alt="image" src="https://user-images.githubusercontent.com/80039707/228282322-95af56d9-d037-42cf-b394-96e0cd2fe2c9.png">
Weak enhancer. Чаще всего находятся на ядерной ламине, так же попадает на RefSeqExon и RefSeqTES.

### Тип 4
<img width="954" alt="image" src="https://user-images.githubusercontent.com/80039707/228287294-a6dfb13b-57f3-4227-a60f-a165e17a7a2a.png">
Weak transcribed. Находится на RefSeqGen, RefSeqTES и RefSeqExon. Выражен на H3k36me3. Попадает на экзон или интрон.

### Тип 5
<img width="955" alt="image" src="https://user-images.githubusercontent.com/80039707/228285934-edc751e8-bda4-41cb-a33e-ff3fccfaa376.png">
Weak transcribed. Находится на RefSeqGen. Выражен на H3k79me2 и H3k36me3. Чаще всего попадает на ген.

### Тип 6
<img width="957" alt="image" src="https://user-images.githubusercontent.com/80039707/228290908-3d818eca-0918-4e13-8a4d-2a037bc1325b.png">
Weak enhancer. Выражен на H3k79me2 и H3k04me1. Преимущественно находится на RefSeqGene. Попадает на интрон.

### Тип 7
<img width="975" alt="image" src="https://user-images.githubusercontent.com/80039707/228272027-2c8dd969-50d5-439f-951f-2bcaec6c82a0.png">
Weak enhancer. Выражен в H3k04me1, H2AFZ. Попадает на RefSeqTES или ламину.

### Тип 8
<img width="954" alt="image" src="https://user-images.githubusercontent.com/80039707/228271397-489583d9-f274-4d87-8db2-9f3fcc488e76.png">
Active Promoter. Находится вблизи CPG островков. Выражен в H3k04me1, H3k04me2, H2AFZ. Попадает на интрон или экзон.

### Тип 9
<img width="954" alt="image" src="https://user-images.githubusercontent.com/80039707/228273117-69a1ed77-5fe9-4b11-a1cc-84cd11557a0a.png">
Active Promoter. Находится вблизи CPG островков. Выражен в H3k04me1, H3k04me2, H3k09ac, H3k27ac, H3k04me3. Попадает на интрон или экзон.

### Тип 10
<img width="958" alt="image" src="https://user-images.githubusercontent.com/80039707/228284003-90f1f512-67f6-4553-87c6-16c6035034ee.png">
Weak transcribed. Чаще всего находятся на RefSeqGene, а также на RefSeqTES и RefSeqExon. Выражен в H3k79me2, H3k04me1, H3k04me2, H3k04me3, H3k09ac, H3k27ac. Попадает на интрон или экзон.

## Бонус

Код находится в collab
<img width="958" alt="image" src="https://user-images.githubusercontent.com/80039707/228298493-1c91c195-9328-4271-bea2-3835bf21b7dd.png">
