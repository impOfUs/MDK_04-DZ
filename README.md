public class Main {
    public static void main(String[] args) {

//(дз номер 1)      

        Phone phone1 = new Phone("89045928544", "IPhon ProMax", 100);
        Phone phone2 = new Phone("89106353488", "Samsung Galaxy S4", 120);
        Phone phone3 = new Phone("89106746481", "Xiaomi Redmi 4A", 150);

        phone1.receiveCall("Катя Tele2");
        System.out.println(phone1.GetNumber());
        phone2.receiveCall("Мама МТС");
        System.out.println(phone2.GetNumber());
        phone3.receiveCall("Кто-то из школы");
        System.out.println(phone3.GetNumber());

        phone1.receiveCall("Катя Tele2", "89045928544");
        phone2.receiveCall("Мама МТС", "89106353488");
        phone3.receiveCall(""Кто-то из школы", "89106746481");

        String[] nums = new String[] {"89045928544", "89106353488", "89106746481"};
        Phone.sendMessage(nums);
        System.out.println("");

//(дз номер 2)

        Person anyName = new Person();

        Person Vad = new Person("Орел Вадим Юрьевич", 18);

        Vad.move(Vad.fullName);
        VAD.talk(Vad.fullName);

    }
}

//(к дз№1 класс phone(отдельно от кода выше))

public class Phone {

    String phone;
    String model;
    int weight;

    public Phone(String phoneNumber, String modelNumber, int phWeight){
        this(phoneNumber, modelNumber);
        weight = phWeight;
    }

    public Phone(String phoneNumber, String modelNumber){
        phone = phoneNumber;
        model = modelNumber;
    }

    public Phone(){}

    public String GetNumber(){
        return phone;
    }

    public void receiveCall(String name){
        System.out.println("Входящий вызов от " + name);
    }

    public void receiveCall(String name, String phoneNumber){
        System.out.println("Входящий вызов от " + name + " с номером " + phoneNumber);
    }

    public static void sendMessage(String[] numbers){
        System.out.println("Вы отправили сообщения на следующие номера: ");
        for (String number : numbers) {
            System.out.print(number + " ");
        }
    }
}

//(к дз№2 класс person(отдельно от кода выше))

public class Person {

    String fullName;
    int age;

    public Person(){}

    public Person(String Fio, int age_person){
        fullName = Fio;
        age = age_person;
    }

    public void move(String name){
        System.out.println(name + " идет.");
    }

    public void talk(String name){
        System.out.println(name + " говорит.");
    }
}

//(дз номер 3, времена года(отдельный проект))

public class Sesons {
    private String[] seasons = new String[]{"Зима", "Весна", "Лето", "Осень"};
    public String bestSeason;

    public Sesons(String best){
        bestSeason = best;
    }
}# MDK_04-DZ
