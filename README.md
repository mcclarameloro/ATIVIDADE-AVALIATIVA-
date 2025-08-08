public class Main {

    static class Aluno {
        String nome;
        int cargaHorariaConcluida;

        Aluno(String nome, int cargaHorariaConcluida) {
            this.nome = nome;
            this.cargaHorariaConcluida = cargaHorariaConcluida;
        }
    }

    public static void main(String[] args) {
        Aluno[] alunos = {
            new Aluno("Alice", 75),
            new Aluno("Nicolle", 70),
            new Aluno("Luana", 80),
            new Aluno("Guilherme", 76),
            new Aluno("Whendell", 90),
        };

        System.out.println("Alunos com mais de 60 horas concluídas:");
        for (int i = 0; i < alunos.length; i++) {
            if (alunos[i].cargaHorariaConcluida > 60) {
                System.out.println("- " + alunos[i].nome +
                                   " (" + alunos[i].cargaHorariaConcluida + " horas)");
            }
        }

        int somaHoras = 0;
        for (int i = 0; i < alunos.length; i++) {
            somaHoras += alunos[i].cargaHorariaConcluida;
        }

        double mediaHoras = (double) somaHoras / alunos.length;
        System.out.printf("\nMédia de horas concluídas: %.2f horas\n", mediaHoras);
    }
}
