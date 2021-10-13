# PovRay-Pendulo
PovRay Pendulo

#include "colors.inc" 
#include "textures.inc"
#include "shapes.inc"

background {color SkyBlue}

camera {
        
        location <8,6,-8>
        look_at <0,2,0>
        }
        
light_source {< 10,8,-20> color White}
light_source {< 4,10,-4> color White}

plane {
        <0,1,0>,-.5
        pigment{ checker color Red color Yellow }
        }
        
union {
        sphere{<-5,0,0>.1}
        cylinder{<0,0,0>, <-5,0,0>, .05}
        pigment{color Silver}
        finish{Metal}
        rotate z*30
        rotate z*120*clock
        translate y*6
        }
        
sphere{ <0,6,0>, .2
        pigment{color Silver}
        finish{Metal}
        }

cylinder{ <0,6,0.1>, <0,6,2>, .3
        texture {Dark_Wood}
        }
sphere{ <0,6,2>, .3


        }
cylinder{ <0,6,2>, <0,.2,2>, .3
        texture {Dark_Wood}
        }
cylinder{ <0,0,2>, <0,.2,2>, 1.5
        texture {Dark_Wood}
        }
