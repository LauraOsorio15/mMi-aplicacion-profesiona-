# mMi-aplicacion-profesiona-
public class AirQuality {
    private String location;
    private int airQualityIndex;

    public AirQuality(String location, int airQualityIndex) {
        this.location = location;
        this.airQualityIndex = airQualityIndex;
    }

    // Getters y setters
}
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.PathVariable;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RestController;

@RestController
@RequestMapping("/api/air-quality")
public class AirQualityController {

    @GetMapping("/{location}")
    public AirQuality getAirQuality(@PathVariable String location) {
        // Aquí se simularía la obtención de datos reales sobre la calidad del aire
        // Puedes conectar aquí con servicios externos o bases de datos reales
        // En este caso, se utilizan datos simulados
        return new AirQuality(location, 80);
    }
}
public class SustainableTip {
    private String tip;

    public SustainableTip(String tip) {
        this.tip = tip;
    }

    // Getters y setters
}
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RestController;

@RestController
@RequestMapping("/api/sustainable-tips")
public class SustainableTipController {

    @GetMapping
    public SustainableTip getSustainableTip() {
        // Aquí se simularía la obtención de datos reales sobre consejos sostenibles
        // Puedes conectar aquí con servicios externos o bases de datos reales
        // En este caso, se utilizan datos simulados
        return new SustainableTip("Recicla tus residuos para reducir la contaminación");
    }
}
