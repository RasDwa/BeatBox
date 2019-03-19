import javax.sound.midi.*;
public class MimiMimiMusicApp {
    public static void main(String args[]) {
        MimiMimiMusicApp mini = new MimiMimiMusicApp();
        mini.play();
        }
        
        public void play() {
            try {
                Sequncer player = MidiSystem.getSequencer();
                player.open();
                Sequence seq = new Sequence(Sequence.PPQ, 4);
                Track track = new Track();
                ShortMassage a = new ShortMassage();
                a.setMassage(144,1,44,100);
                MidiEvent noteOn = new MidiEvent(a, 1);
                
                ShortMassage b = new ShortMassage();
                a.setMassage(128,1,44,100);
                MidiEvent noteOn = new MidiEvent(b, 16);
                
                player.setSequece(seq);
                
                player.stert();
            }
            catch (Exception ex) {
                ex.printStackTrace();
            }
        }
}
