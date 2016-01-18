# Approach...

    cat gdp.manifest | sort | uniq | sed "s/ cortexa15hf-vfp-neon / /" |sed "s/ core2-64 / /" > gdp.sorted
    cat agl.manifest | sort | uniq | sed "s/ qemux86_64 / /" |sed "s/ core2-64 / /" > agl.sorted
    comm agl.sorted gdp.sorted | sort > comm-output.txt
