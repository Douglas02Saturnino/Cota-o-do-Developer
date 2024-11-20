<script>
    let profile = {
        name: "Douglas Saturnino",
        avatar: "htpps://github.com/maykbrito.png",
        valueHour: Number(75).toLocaleString('pt-BR', {
            style: 'currency',
            currency: 'BRL'
        }),
        monthlyIncome: 5000,
        hoursPerDay: 16,
        dayAWeek: 6,
        vacationWeeks: 4,
    }
</script>

<div class="container animete-up delay-2 flex justify-between bg-gray-100 w-full">
    <aside class="card max-w-48 bg-white border border-gray-200">
        <img src={ profile.avatar } alt={ profile.name }>
        <h2>{ profile.name }</h2>
        <p>
            O valor da sua hora é <br/>
            <strong>{profile.valueHour}</strong>
        </p>
    </aside>

<main>
    <form>
        <fieldset>
            <legend> Dados do perfil</legend>
            <div class="separator light"></div>
            <div class="input-group">
                <div class="input-wrapper">
                    <label for="name">Nome</label>
                    <input type="text" id="name" value={profile.name} />
                </div>
                <div class="inputi-wrapper">
                    <label for="avatar">Link da foto</label>
                    <input placeholder="https://" type="url" id="avatar" name="avatar" 
                    value={profile.avatar}/>
                </div>
            </div>
        </fieldset>
        <fieldset>
            <legend>Planejamento</legend>
            <div class="separator light"> </div>
            <div class="input-group">
                <div class="input-wrapper">
                    <label for="monthly-budget">Quanto eu <br/>quero ganhar por mês?</label>
                    <input type="amount" step="0.1" id="monthly-budget" name="monthly-budget"
                    placeholder="R$" value={profile.monthlyIncome}/>
                </div>
                <div class="input-wrapper">
                    <label for="hours-per-day">Quanto horas <br/>quero trabalhar por dia?</label>
                    <input type="number" id="hours-per-day" name="hours-per-day"
                    value={profile.valueHour}/>
                </div>
                <div class="input-group">
                    <div class="input-wrapper">
                    <label for="days-per-week">Quanto dias <br/>quero trabalhar por semana?</label>
                    <input type="number" id="days-per-week" name="days-per-week"
                    value={profile.daysAWeek}/>
                </div>
                <div class="input-wrapper">
                    <label for="vacation-per-year">Quantas semanas <br/> por ano você quer tirar férias</label>
                    <input type="number" id="vacation-per-year" name="vacation-per-year"
                    value={profile.vacationWeeks}/>
                </div>
            </div>
        </fieldset>
    </form>
</main>    
</div>