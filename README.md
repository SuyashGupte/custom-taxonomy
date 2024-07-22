#  InstructLab with custom taxonomy

## Follow these steps to setup this repo as your taxonomy for instructlab

1. Make a folder called instructlab(or any name) in your working directory.
    ```
    mkdir instructlab
    cd instructlab
    ```
2. Clone this repo in your project directory.
    ```
    git clone https://github.com/SuyashGupte/custom-taxonomy.git
    ```
3. Create a virtual env and install instructlab.
   ```
   python3 -m venv venv
   source venv/bin/activate
   pip install instructlab
   ```
4. Initialize instructlab
   ```
   ilab config init
   ```
   and give the Path to taxonomy repo as `custom-taxonomy`.
5. Run the ilab diff command to check if taxonomy is getting correctly identified.
   ```
   ilab taxonomy diff
   ```
6. To test the taxonomy add this qna.yaml to given path and run ilab diff.
   ```
   touch custom-taxonomy/compositional_skills/sports/cricket/highlights_generation/qna.yaml
   ```
   Add the content of `sample.yaml` in the `qna.yaml`. Then run
   ```
   ilab taxonomy diff
   ```
7. You should see this text.</br>
   _compositional_skills/sports/cricket/highlights_generation/qna.yaml_</br>
   _Taxonomy in custom-taxonomy is valid :)_
