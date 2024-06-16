## Hi there 👋 I am Aly

```java
public class Aly
{
  Pronouns pronouns;
  String linkedInUrl;
  String [] tools = {"Unity", "React", "VS Code", ".NET"};
  String [] programmingLanguages = {"Java", "HTML", "CSS", "JavaScript", "C#", "C", "Python", "SQL"};
  String [] hackathonsParticipations = {"KnightHacks", "HackJam", "Hacklytics"};

  public Aly()
  {
    this.pronouns = new Pronouns("she", "her", "her", "hers", "herself");
    this.linkedInUrl = "https://www.linkedin.com/in/alyshairvin/";
  }

  public void greet()
  {
    System.out.println("Hi there 👋 I am Aly");
    System.out.println("My pronouns are " + pronouns.subject + "/" + pronouns.object + "/" + pronouns.possessivePronoun + ".");
    System.out.println("You can find me on LinkedIn: " + linkedInUrl);
    System.out.println("Here are some tools I use: " + String.join(", ", tools));
    System.out.println("I am proficient in the following programming languages: " + String.join(", ", programmingLanguages));
    System.out.println("I have participated in these hackathons: " + String.join(", ", hackathonsParticipations));
    System.out.println("It is very nice to meet you!");
  }

  public static void main(String [] args)
  {
    Aly aly = new Aly();
    aly.greet();
  }
}

class Pronouns
{
  String subject;
  String object;
  String possessive;
  String possessivePronoun;
  String reflexive;

  public Pronouns(String subject, String object, String possessive, String possessivePronoun, String reflexive)
  {
    this.subject = subject;
    this.object = object;
    this.possessive = possessive;
    this.possessivePronoun = possessivePronoun;
    this.reflexive = reflexive;
  }

  public Pronouns(String [] pronouns)
  {
    if (pronouns.length != 5)
    {
      throw new IllegalArgumentException("Too many or not enough pronouns");
    }

    this.subject = pronouns[0];
    this.object = pronouns[1];
    this.possessive = pronouns[2];
    this.possessivePronoun = pronouns[3];
    this.reflexive = pronouns[4];
  }
}
```
