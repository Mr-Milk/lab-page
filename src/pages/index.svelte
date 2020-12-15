<script>
    import {Container, Card, CardText,} from 'svelte-materialify'
    let home_img = "images/home-transcription.jpg"
</script>

<style>

    img{
        margin: 0;
        max-width:100%;
        max-height:100%
    }

    .title {
        font-family: Arial, serif;
        font-size: 25px;
    }

    .text {
        text-align: left;
        font-size: 16px;
        line-height: 2.3;
    }

    @media (max-width: 640px) {
        .text {
            text-align: left;
            font-size: 12px;
            line-height: 1.5;
        }
    }

</style>

<Container class="align-center" style="text-align: center;">

    <span>
            <img src={home_img} alt="transcription factor">
    </span>

    <div class="d-flex justify-center mt-4 mb-4">
    <Card outlined style="max-width:800px;">
        <div class="pl-4 pr-4 pt-3">
            <span class="text-h5 mb-2 title">LAB RESEARCH</span>
            <br />
        </div>
        <CardText style="font-size: 14px;line-height: 2.3; color: #333;">
            My lab is interested in understanding the molecular details of nuclear hormone signaling and how
            these pathways relate to disease conditions, including cancers.
            Currently, we are investigating how lipophilic hormones such as estrogens and androgens regulate
            the transcriptional activities of nuclear hormone receptors in the context of a chromatin environment.
            We employ a combination of powerful biological tools, including modern genetic and cell-based techniques
            (RNAi, ChIP, and FISH) and next-generation sequencing approaches (ChIP-Seq, RNA-Seq, and ChIA-PET),
            to define the molecular mechanisms of transcriptional regulation by estrogen and androgen receptors.
            The findings from our work will have direct impact towards the development of therapeutic targets for the
            wide range of diseases and disorders in which these and other nuclear receptors play a role.
        </CardText>
    </Card>
    </div>
</Container>
