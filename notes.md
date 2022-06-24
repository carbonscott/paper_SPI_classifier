## Two aspects of the challenge to tackle

- For a run-specific model, we want to train a good model with as few examples
  as possible.

- Can the model be generalized so that it could work for different runs?
  (define run better here, experiments with different particles)

the model still demands too many labeled images to train.  Is there a better way?

propose a model that only requires a few dozen labeled images per class to train
narrowing the gap in its application in.


## Story on datasets

Currently avaiable SPI datasets (non-labeled), no labeled SPI datasets have been
publicly available.

```
cxidb_id,method,lightsource,sample
001,Single Particle X-ray Diffraction Imaging,LCLS,Mimivirus
002,Single Particle X-ray Diffraction Imaging,LCLS,Mimivirus
010,Single Particle X-ray Diffraction Imaging,LCLS,Nanorice
011,Single Particle X-ray Diffraction Imaging,LCLS,Magnetosomes
012,Single Particle X-ray Diffraction Imaging,LCLS,Tobacco mosaic virus
013,Single Particle X-ray Diffraction Imaging,LCLS,T4 bacteriophage
014,Single Particle X-ray Diffraction Imaging,LCLS,Paramecium bursaria Chlorella virus
019,Single Particle X-ray Diffraction Imaging,LCLS,Airborne Particulate Matter (Soot)
020,Single Particle X-ray Diffraction Imaging,LCLS,Clusters of Polystyrene Spheres
025,Single Particle X-ray Diffraction Imaging,LCLS,Carboxysomes
026,Single Particle X-ray Diffraction Imaging,LCLS,Cyanobium gracile
027,Single Particle X-ray Diffraction Imaging,LCLS,Synechococcus elongatus
030,Single Particle X-ray Diffraction Imaging,LCLS,Mimivirus
036,Single Particle X-ray Diffraction Imaging,LCLS,Rice Dwarf Virus
037,Single Particle X-ray Diffraction Imaging,LCLS,Cyanobium gracile and Synechococcus elongtatus
056,Single Particle X-ray Diffraction Imaging,LCLS,Omono River Virus
057,Single Particle X-ray Diffraction Imaging,LCLS,Gold core and palladium shell nanoparticles
058,Single Particle X-ray Diffraction Imaging,LCLS,Coliphage PR772
078,Single Particle X-ray Diffraction Imaging,LCLS,RNA polymerase II
088,Single Particle X-ray Diffraction Imaging,LCLS,PR772
119,Single Particle X-ray Diffraction Imaging,LCLS,Sucrose
155,Single Particle X-ray Diffraction Imaging,LCLS,Melbournevirus
156,Single Particle X-ray Diffraction Imaging,LCLS,Coliphage PR772
```


### Resources

- Exp           : `amo10510`, `amo15010`
- Raw data (cxi): `/reg/data/ana03/scratch/cwang31/amo10510`
- GUI launcher  : `/reg/data/ana03/scratch/cwang31/play/hit-labeler`
- Metadata: [link](https://docs.google.com/spreadsheets/d/1AM47pHdIfCe45-wn4MjE8a67Pk8GzzltmJoZdE4XVUw/edit?hl=en_US&hl=en_US#gid=0)


### Contents in `amo10510`

```
cxidb,exp                                      ,light source,sample                             ,number of snapshots
010  ,Single Particle X-ray Diffraction Imaging,LCLS        ,Nanorice                           ,9302
011  ,Single Particle X-ray Diffraction Imaging,LCLS        ,Magnetosomes                       ,2981
012  ,Single Particle X-ray Diffraction Imaging,LCLS        ,Tobacco mosaic virus               ,532
013  ,Single Particle X-ray Diffraction Imaging,LCLS        ,T4 bacteriophage                   ,18925
014  ,Single Particle X-ray Diffraction Imaging,LCLS        ,Paramecium bursaria Chlorella virus,880
```


## Open questions

- What accuracy is good enough for SPI reconstruction? 

- What is the latency of our ML model? To run on 1MHz timescale, we want to
  process images at fraction of milliseconds.


## More resources

- amo86615
  - https://cxidb.org/id-156.html
- amox34117
  - https://cxidb.org/id-58.html
  - https://www.nature.com/articles/sdata201779/tables/2
