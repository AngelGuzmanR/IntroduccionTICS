import java.io.FileWriter;
import java.io.IOException;
import java.util.Scanner;

public class CurriculumVitae {

    public static void main(String[] args) {
        // Crear escáner para leer la entrada del usuario
        Scanner scanner = new Scanner(System.in);
        
        // Variables para los datos del CV
        String nombre, direccion, telefono, email, educacion, experiencia, habilidades;
        
        // Solicitar datos del usuario
        System.out.println("Ingrese su nombre completo: ");
        nombre = scanner.nextLine();
        
        System.out.println("Ingrese su dirección: ");
        direccion = scanner.nextLine();
        
        System.out.println("Ingrese su número de teléfono: ");
        telefono = scanner.nextLine();
        
        System.out.println("Ingrese su email: ");
        email = scanner.nextLine();
        
        System.out.println("Ingrese su formación académica: ");
        educacion = scanner.nextLine();
        
        System.out.println("Ingrese su experiencia laboral: ");
        experiencia = scanner.nextLine();
        
        System.out.println("Ingrese sus habilidades: ");
        habilidades = scanner.nextLine();
        
        // Crear el contenido del CV
        String curriculum = "Curriculum Vitae\n" +
                            "-----------------\n" +
                            "Nombre: " + nombre + "\n" +
                            "Dirección: " + direccion + "\n" +
                            "Teléfono: " + telefono + "\n" +
                            "Email: " + email + "\n" +
                            "\nFormación Académica:\n" + educacion + "\n" +
                            "\nExperiencia Laboral:\n" + experiencia + "\n" +
                            "\nHabilidades:\n" + habilidades + "\n";
        
        // Guardar el CV en un archivo
        try {
            FileWriter writer = new FileWriter("CurriculumVitae.txt");
            writer.write(curriculum);
            writer.close();
            System.out.println("El currículum ha sido guardado correctamente en 'CurriculumVitae.txt'.");
        } catch (IOException e) {
            System.out.println("Ocurrió un error al guardar el currículum.");
            e.printStackTrace();
        }
        
        // Cerrar el escáner
        scanner.close();
    }
}

