## 共通

* object1.velocity=0.0e0, -3.0e-1, 0.0e0



## vacuum vs air

* demonly



## density comparison

* Particle.Density



## various density

### Layer

#### Initial

* particletype0.density (下)
* particletype1.density
* object1.move=no
* demonly=yes
* IterationsTotal:30000

#### DEM

* object1.move=yes
* IterationsTotal:120000
* Initialから初期配置コピー

#### CFD

* object1.move=yes
* demonly=no
* IterationsTotal:120000
* Initialから初期配置コピー



### Random

#### InitialSameDensity(既存のものを使いまわせる)

* particletype0.density=1500
* particletype1.density=1500
* object1.move=no
* demonly=yes
* Iterations.Total: 200000

#### Initial

* particletype0.density=(righter layer particle Density)
* particletype1.density=(heavier layer particle Density)
* Iterations.Total: 20000（桁数注意）
* InitialSameDensityから初期配置コピー

#### DEM

- object1.move=yes
- IterationsTotal:120000
- Initialから初期配置コピー

#### CFD

- object1.move=yes
- demonly=no
- IterationsTotal:120000
- Initialから初期配置コピー

