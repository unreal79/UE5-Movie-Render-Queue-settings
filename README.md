# UE5-Movie-Render-Queue-settings

These are UE5 Movie Render Queue setting for ray-tracing rendering.

## How to setup

1. Enable plugin "Movie Render Queue" (and later use it to render movies). Restart UE5.

2. Copy "MoviePipelinePrimaryConfig.uasset" file to "Content" dir of your project. 

3. Edit it to your liking: primarily "Output Resolution", "Temporal Sample Count". If you chose to enable "Anti Aliasing Method", increase "Spatial Sample Count".

4. Recommended: copy and paste (Ctrl+V) the text (PostProcessVolume) in UE5 editor:
 ```
Begin Map
   Begin Level
      Begin Actor Class=/Script/Engine.PostProcessVolume Name=PostProcessVolume_0 Archetype="/Script/Engine.PostProcessVolume'/Script/Engine.Default__PostProcessVolume'" ExportPath="/Script/Engine.PostProcessVolume'/Game/MyProject/MyProject.MyProject:PersistentLevel.PostProcessVolume_0'"
         Begin Object Class=/Script/Engine.BrushComponent Name="BrushComponent0" Archetype="/Script/Engine.BrushComponent'/Script/Engine.Default__PostProcessVolume:BrushComponent0'" ExportPath="/Script/Engine.BrushComponent'/Game/MyProject/MyProject.MyProject:PersistentLevel.PostProcessVolume_0.BrushComponent0'"
            Begin Object Class=/Script/Engine.BodySetup Name="BodySetup_0" ExportPath="/Script/Engine.BodySetup'/Game/MyProject/MyProject.MyProject:PersistentLevel.PostProcessVolume_0.BrushComponent0.BodySetup_0'"
            End Object
         End Object
         Begin Object Class=/Script/UnrealEd.CubeBuilder Name="CubeBuilder_3" ExportPath="/Script/UnrealEd.CubeBuilder'/Game/MyProject/MyProject.MyProject:PersistentLevel.PostProcessVolume_0.CubeBuilder_3'"
         End Object
         Begin Brush Name=Model_1
         End Brush
         Begin Object Name="BrushComponent0" ExportPath="/Script/Engine.BrushComponent'/Game/MyProject/MyProject.MyProject:PersistentLevel.PostProcessVolume_0.BrushComponent0'"
            Begin Object Name="BodySetup_0" ExportPath="/Script/Engine.BodySetup'/Game/MyProject/MyProject.MyProject:PersistentLevel.PostProcessVolume_0.BrushComponent0.BodySetup_0'"
               AggGeom=(ConvexElems=((VertexData=((X=-100.000000,Y=100.000000,Z=-100.000000),(X=-100.000000,Y=100.000000,Z=100.000000),(X=-100.000000,Y=-100.000000,Z=100.000000),(X=-100.000000,Y=-100.000000,Z=-100.000000),(X=100.000000,Y=100.000000,Z=-100.000000),(X=100.000000,Y=100.000000,Z=100.000000),(X=100.000000,Y=-100.000000,Z=-100.000000),(X=100.000000,Y=-100.000000,Z=100.000000)),IndexData=(5,4,1,0,2,1,0,1,4,3,0,4,3,2,0,6,3,4,6,2,3,5,1,2,5,6,4,7,5,2,7,6,5,7,2,6),ElemBox=(Min=(X=-100.000000,Y=-100.000000,Z=-100.000000),Max=(X=100.000000,Y=100.000000,Z=100.000000),IsValid=True))))
               bGenerateMirroredCollision=False
               CollisionTraceFlag=CTF_UseSimpleAsComplex
            End Object
            Brush="/Script/Engine.Model'Model_1'"
            BrushBodySetup="/Script/Engine.BodySetup'BodySetup_0'"
            BodyInstance=(MaxAngularVelocity=3599.999756)
            RelativeLocation=(X=0.000000,Y=0.000000,Z=1000.000000)
         End Object
         Begin Object Name="CubeBuilder_3" ExportPath="/Script/UnrealEd.CubeBuilder'/Game/MyProject/MyProject.MyProject:PersistentLevel.PostProcessVolume_0.CubeBuilder_3'"
            Vertices(0)=(X=-100.000000,Y=-100.000000,Z=-100.000000)
            Vertices(1)=(X=-100.000000,Y=-100.000000,Z=100.000000)
            Vertices(2)=(X=-100.000000,Y=100.000000,Z=-100.000000)
            Vertices(3)=(X=-100.000000,Y=100.000000,Z=100.000000)
            Vertices(4)=(X=100.000000,Y=-100.000000,Z=-100.000000)
            Vertices(5)=(X=100.000000,Y=-100.000000,Z=100.000000)
            Vertices(6)=(X=100.000000,Y=100.000000,Z=-100.000000)
            Vertices(7)=(X=100.000000,Y=100.000000,Z=100.000000)
            Polys(0)=(VertexIndices=(0,1,3,2),Direction=1)
            Polys(1)=(VertexIndices=(2,3,7,6),Direction=1)
            Polys(2)=(VertexIndices=(6,7,5,4),Direction=1)
            Polys(3)=(VertexIndices=(4,5,1,0),Direction=1)
            Polys(4)=(VertexIndices=(3,1,5,7),Direction=1)
            Polys(5)=(VertexIndices=(0,2,6,4),Direction=1)
            Layer="Cube"
         End Object
         Settings=(bOverride_ColorContrast=True,bOverride_ColorGamma=True,bOverride_ColorOffset=True,bOverride_SceneFringeIntensity=True,bOverride_BloomMethod=True,bOverride_BloomIntensity=True,bOverride_BloomThreshold=True,bOverride_BloomConvolutionScatterDispersion=True,bOverride_AutoExposureMethod=True,bOverride_AutoExposureBias=True,bOverride_AutoExposureApplyPhysicalCameraExposure=True,bOverride_LocalExposureDetailStrength=True,bOverride_LensFlareIntensity=True,bOverride_VignetteIntensity=True,bOverride_MotionBlurAmount=True,bOverride_MotionBlurMax=True,bOverride_MotionBlurTargetFPS=True,bOverride_ReflectionMethod=True,bOverride_LumenReflectionQuality=True,bOverride_RayTracingReflectionsMaxRoughness=True,bOverride_RayTracingReflectionsMaxBounces=True,bOverride_RayTracingReflectionsSamplesPerPixel=True,bOverride_RayTracingReflectionsShadows=True,bOverride_TranslucencyType=True,bOverride_DynamicGlobalIlluminationMethod=True,bOverride_LumenSceneLightingQuality=True,bOverride_LumenSceneDetail=True,bOverride_LumenSceneViewDistance=True,bOverride_LumenFinalGatherQuality=True,bOverride_LumenSkylightLeaking=True,bOverride_LumenRayLightingMode=True,bOverride_RayTracingGI=True,bOverride_RayTracingGIMaxBounces=True,bOverride_RayTracingGISamplesPerPixel=True,BloomMethod=BM_FFT,AutoExposureMethod=AEM_Manual,ColorSaturation=(X=0.800000,Y=0.800000,Z=1.200000,W=1.000000),ColorContrast=(X=1.200000,Y=1.200000,Z=1.200000,W=1.000000),ColorGamma=(X=0.900000,Y=0.900000,Z=0.900000,W=1.000000),ColorOffset=(X=-0.020000,Y=-0.010000,Z=0.000000,W=0.000000),BloomIntensity=4.000000,BloomConvolutionScatterDispersion=0.500000,DynamicGlobalIlluminationMethod=RayTraced,LumenSceneLightingQuality=2.000000,LumenSceneDetail=4.000000,LumenFinalGatherQuality=10.000000,LumenSkylightLeaking=0.100000,RayTracingGIType=BruteForce,RayTracingGIMaxBounces=3,ReflectionMethod=RayTraced,LumenReflectionQuality=2.000000,LumenRayLightingMode=HitLighting,RayTracingReflectionsMaxBounces=2,RayTracingReflectionsSamplesPerPixel=2,AutoExposureApplyPhysicalCameraExposure=False,LocalExposureDetailStrength=1.200000,LensFlareIntensity=0.000000)
         bUnbound=True
         BrushType=Brush_Add
         Begin Brush Name=Model_1
            Begin PolyList
               Begin Polygon Link=0
                  Origin   -00100.000000,-00100.000000,-00100.000000
                  Normal   -00001.000000,+00000.000000,+00000.000000
                  TextureU +00000.000000,+00001.000000,+00000.000000
                  TextureV +00000.000000,+00000.000000,-00001.000000
                  Vertex   -00100.000000,-00100.000000,-00100.000000
                  Vertex   -00100.000000,-00100.000000,+00100.000000
                  Vertex   -00100.000000,+00100.000000,+00100.000000
                  Vertex   -00100.000000,+00100.000000,-00100.000000
               End Polygon
               Begin Polygon Link=1
                  Origin   -00100.000000,+00100.000000,-00100.000000
                  Normal   +00000.000000,+00001.000000,+00000.000000
                  TextureU +00001.000000,-00000.000000,+00000.000000
                  TextureV +00000.000000,+00000.000000,-00001.000000
                  Vertex   -00100.000000,+00100.000000,-00100.000000
                  Vertex   -00100.000000,+00100.000000,+00100.000000
                  Vertex   +00100.000000,+00100.000000,+00100.000000
                  Vertex   +00100.000000,+00100.000000,-00100.000000
               End Polygon
               Begin Polygon Link=2
                  Origin   +00100.000000,+00100.000000,-00100.000000
                  Normal   +00001.000000,+00000.000000,+00000.000000
                  TextureU +00000.000000,-00001.000000,+00000.000000
                  TextureV +00000.000000,+00000.000000,-00001.000000
                  Vertex   +00100.000000,+00100.000000,-00100.000000
                  Vertex   +00100.000000,+00100.000000,+00100.000000
                  Vertex   +00100.000000,-00100.000000,+00100.000000
                  Vertex   +00100.000000,-00100.000000,-00100.000000
               End Polygon
               Begin Polygon Link=3
                  Origin   +00100.000000,-00100.000000,-00100.000000
                  Normal   +00000.000000,-00001.000000,+00000.000000
                  TextureU -00001.000000,-00000.000000,-00000.000000
                  TextureV +00000.000000,+00000.000000,-00001.000000
                  Vertex   +00100.000000,-00100.000000,-00100.000000
                  Vertex   +00100.000000,-00100.000000,+00100.000000
                  Vertex   -00100.000000,-00100.000000,+00100.000000
                  Vertex   -00100.000000,-00100.000000,-00100.000000
               End Polygon
               Begin Polygon Link=4
                  Origin   -00100.000000,+00100.000000,+00100.000000
                  Normal   +00000.000000,+00000.000000,+00001.000000
                  TextureU +00001.000000,+00000.000000,+00000.000000
                  TextureV +00000.000000,+00001.000000,+00000.000000
                  Vertex   -00100.000000,+00100.000000,+00100.000000
                  Vertex   -00100.000000,-00100.000000,+00100.000000
                  Vertex   +00100.000000,-00100.000000,+00100.000000
                  Vertex   +00100.000000,+00100.000000,+00100.000000
               End Polygon
               Begin Polygon Link=5
                  Origin   -00100.000000,-00100.000000,-00100.000000
                  Normal   +00000.000000,+00000.000000,-00001.000000
                  TextureU +00001.000000,+00000.000000,+00000.000000
                  TextureV +00000.000000,-00001.000000,+00000.000000
                  Vertex   -00100.000000,-00100.000000,-00100.000000
                  Vertex   -00100.000000,+00100.000000,-00100.000000
                  Vertex   +00100.000000,+00100.000000,-00100.000000
                  Vertex   +00100.000000,-00100.000000,-00100.000000
               End Polygon
            End PolyList
         End Brush
         Brush="/Script/Engine.Model'Model_1'"
         BrushComponent="BrushComponent0"
         BrushBuilder="/Script/UnrealEd.CubeBuilder'CubeBuilder_3'"
         bHidden=False
         SpawnCollisionHandlingMethod=AlwaysSpawn
         RootComponent="BrushComponent0"
         ActorLabel="PostProcessVolume"
         FolderPath="Lighting"
         bIsSpatiallyLoaded=False
      End Actor
   End Level
Begin Surface
End Surface
End Map
 ```
