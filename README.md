graph TD
    A[frontend/] --> B[lib/]
    A --> C[android/]
    A --> D[ios/]
    
    B --> E[main.dart]
    
    E --> F[MyApp]
    F --> G[MyHomePage]
    G --> H[_MyHomePageState]
    
    C --> I[AndroidManifest.xml]
    I --> J[Permissions]
    J --> J1[ACCESS_FINE_LOCATION]
    J --> J2[ACCESS_COARSE_LOCATION]
    J --> J3[INTERNET]
    
    D --> K[Runner/]
    K --> L[Info.plist]
    L --> M[Permissions & Configs]
    M --> M1[Location Usage]
    M --> M2[Naver Map Config]
    
    %% Dependencies
    subgraph Dependencies
        N[pubspec.yaml]
        N --> O[flutter]
        N --> P[naver_map_plugin]
        N --> Q[geolocator]
        N --> R[http]
        N --> S[shared_preferences]
    end
    
    %% Relationships
    E -.-> P
    E -.-> Q
    G -.-> P
    G -.-> Q
