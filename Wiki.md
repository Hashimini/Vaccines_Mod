# Vaccines Project — Wiki

This document lists all vaccines in the mod with their defs and technical values.  
All vaccines below share the same base values (WorkToMake, workAmount, MarketValue, research baseCost, etc.).

---

## Overview (Quick Summary)

| Disease | Vaccine ThingDef | RecipeDef | ResearchProjectDef | Produced At | Ingredients |
|--------:|------------------:|----------:|-------------------:|-------------:|-------------:|
| BloodRot | `Vaccine_BloodRot` | `Produce_Vaccine_BloodRot` | `Vaccines_Unlock_BloodRot` | Drug Lab | 1x HemogenPack, 2x Neutroamine |
| Flu | `Vaccine_Flu` | `Produce_Vaccine_Flu` | `Vaccines_Unlock_Flu` | Drug Lab | 1x HemogenPack, 2x Neutroamine |
| GutWorms | `Vaccine_GutWorms` | `Produce_Vaccine_GutWorms` | `Vaccines_Unlock_GutWorms` | Drug Lab | 1x HemogenPack, 2x Neutroamine |
| Infection | `Vaccine_Infection` | `Produce_Vaccine_Infection` | `Vaccines_Unlock_Infection` | Drug Lab | 1x HemogenPack, 2x Neutroamine |
| Malaria | `Vaccine_Malaria` | `Produce_Vaccine_Malaria` | `Vaccines_Unlock_Malaria` | Drug Lab | 1x HemogenPack, 2x Neutroamine |
| MuscleParasites | `Vaccine_MuscleParasites` | `Produce_Vaccine_MuscleParasites` | `Vaccines_Unlock_MuscleParasites` | Drug Lab | 1x HemogenPack, 2x Neutroamine |
| OrganDecay | `Vaccine_OrganDecay` | `Produce_Vaccine_OrganDecay` | `Vaccines_Unlock_OrganDecay` | Drug Lab | 1x HemogenPack, 2x Neutroamine |
| Plague | `Vaccine_Plague` | `Produce_Vaccine_Plague` | `Vaccines_Unlock_Plague` | Drug Lab | 1x HemogenPack, 2x Neutroamine |
| Scaria | `Vaccine_Scaria` | `Produce_Vaccine_Scaria` | `Vaccines_Unlock_Scaria` | Drug Lab | 1x HemogenPack, 2x Neutroamine |

---

## Shared Structure (applies to all vaccines)

### **ThingDef (item)**
- `WorkToMake`: **1200**
- `MarketValue`: **6000**
- `Mass`: **0.03**
- `stackLimit`: **6**
- `techLevel`: `Industrial`
- `graphicData.texPath`: `Things/Item/Drug/Vaccines/<Vaccine_Name>`
- Ingesting applies a corresponding immunity hediff: `Vaccine_<Disease>_Immunity` (severity 1.0)

### **RecipeDef (crafting)**
- `workAmount`: **4000**
- `workSpeedStat`: `DrugSynthesisSpeed`
- `workSkill`: `Medicine` (requires 14)
- `researchPrerequisite`: `Vaccines_Unlock_<Disease>`
- `recipeUsers`: `DrugLab`
- `ingredients`:  
  - 1x HemogenPack  
  - 2x Neutroamine  
- `products`: 1x `Vaccine_<Disease>`

### **ResearchProjectDef (research)**
- `baseCost`: **650**
- `prerequisites`: `Vaccines_Unlock`
- `techLevel`: `Industrial`

### **HediffDef (immunity)**
- `hediffClass`: `Hediff_High`
- `maxSeverity`: **1.0**
- `severityPerDay`: **-0.0033**
- `makeImmuneTo`: disease matching the vaccine

---

# Individual Vaccine Sections

---

## **Flu**

### ThingDef
- `defName`: `Vaccine_Flu`
- Gives: `Vaccine_Flu_Immunity`
- WorkToMake: 1200  
- MarketValue: 6000  
- Mass: 0.03  
- stackLimit: 6  

### RecipeDef
- `defName`: `Produce_Vaccine_Flu`
- workAmount: 4000  
- Medicine skill 14  
- researchPrerequisite: `Vaccines_Unlock_Flu`  
- ingredients: 1 HemogenPack, 2 Neutroamine  
- product: 1 Vaccine_Flu  

### ResearchProjectDef
- `defName`: `Vaccines_Unlock_Flu`
- baseCost: 650  
- prerequisite: `Vaccines_Unlock`  

### HediffDef
- `defName`: `Vaccine_Flu_Immunity`
- makeImmuneTo: `Flu`

---

## **BloodRot**
### ThingDef
- `Vaccine_BloodRot`  
- Gives `Vaccine_BloodRot_Immunity`  

### RecipeDef
- `Produce_Vaccine_BloodRot`  
- Requires Medicine 14, 1 HemogenPack, 2 Neutroamine  

### ResearchProjectDef
- `Vaccines_Unlock_BloodRot`  

### HediffDef
- `Vaccine_BloodRot_Immunity` → immune to BloodRot

---

## **GutWorms**
### ThingDef
- `Vaccine_GutWorms`  
### RecipeDef
- `Produce_Vaccine_GutWorms`  
### ResearchProjectDef
- `Vaccines_Unlock_GutWorms`  
### HediffDef
- `Vaccine_GutWorms_Immunity` → immune to GutWorms

---

## **Infection**
### ThingDef
- `Vaccine_Infection`  
### RecipeDef
- `Produce_Vaccine_Infection`  
### ResearchProjectDef
- `Vaccines_Unlock_Infection`  
### HediffDef
- `Vaccine_Infection_Immunity` → immune to Infection

---

## **Malaria**
### ThingDef
- `Vaccine_Malaria`  
### RecipeDef
- `Produce_Vaccine_Malaria`  
### ResearchProjectDef
- `Vaccines_Unlock_Malaria`  
### HediffDef
- `Vaccine_Malaria_Immunity` → immune to Malaria

---

## **Muscle Parasites**
### ThingDef
- `Vaccine_MuscleParasites`  
### RecipeDef
- `Produce_Vaccine_MuscleParasites`  
### ResearchProjectDef
- `Vaccines_Unlock_MuscleParasites`  
### HediffDef
- `Vaccine_MuscleParasites_Immunity` → immune to Muscle Parasites

---

## **Organ Decay**
### ThingDef
- `Vaccine_OrganDecay`  
### RecipeDef
- `Produce_Vaccine_OrganDecay`  
### ResearchProjectDef
- `Vaccines_Unlock_OrganDecay`  
### HediffDef
- `Vaccine_OrganDecay_Immunity` → immune to Organ Decay

---

## **Plague**
### ThingDef
- `Vaccine_Plague`  
### RecipeDef
- `Produce_Vaccine_Plague`  
### ResearchProjectDef
- `Vaccines_Unlock_Plague`  
### HediffDef
- `Vaccine_Plague_Immunity` → immune to Plague

---

## **Scaria**
### ThingDef
- `Vaccine_Scaria`  
### RecipeDef
- `Produce_Vaccine_Scaria`  
### ResearchProjectDef
- `Vaccines_Unlock_Scaria`  
### HediffDef
- `Vaccine_Scaria_Immunity` → immune to Scaria
